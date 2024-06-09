# Welcome to my website

This is my personal website and the template is from Saad.

## 1 How to deploy it

To deploy the `build` folder from the `main` branch of your `my-website` repository to the `gh-pages` branch, follow these steps:

### Step 1: Ensure the `build` Folder is Generated and Committed in the `main` Branch

1. Switch to the `main` branch:

    ```bash
    git checkout main
    ```

2. Generate the `build` folder if it’s not already generated:

    ```bash
    npm run build
    ```

3. Commit the `build` folder changes:

    ```bash
    git add build
    git commit -m "Add build folder"
    ```

### Step 2: Switch to the `gh-pages` Branch

Switch to the `gh-pages` branch. If the branch doesn't exist, create it:

```bash
git checkout gh-pages || git checkout -b gh-pages
```

### Step 3: Clear All Files in the `gh-pages` Branch

Clear all files in the `gh-pages` branch:

```bash
git rm -rf .
```

### Step 4: Copy the `build` Folder Content from the `main` Branch

1. Copy the `build` folder content from the `main` branch:

    ```bash
    git checkout main -- build
    ```

2. Copy the content of the `build` folder to the root directory:

    ```bash
    cp -r build/* .
    ```

3. Remove the temporarily copied `build` folder:

    ```bash
    rm -rf build
    ```

### Step 5: Commit and Push Changes to the `gh-pages` Branch

1. Add all changes:

    ```bash
    git add .
    ```

2. Commit the changes:

    ```bash
    git commit -m "Deploy build folder to gh-pages"
    ```

3. Push the changes to the remote `gh-pages` branch:

    ```bash
    git push origin gh-pages --force
    ```

### Full Command Example

Here is the complete sequence of commands:

```bash
# Ensure you are on the main branch and generate the build folder
git checkout main
npm run build

# Commit the build folder changes
git add build
git commit -m "Add build folder"

# Switch to the gh-pages branch, create it if it doesn't exist
git checkout gh-pages || git checkout -b gh-pages

# Clear all files in the gh-pages branch
git rm -rf .

# Copy the build folder content from the main branch
git checkout main -- build
cp -r build/* .
rm -rf build

# Add all changes
git add .

# Commit the changes
git commit -m "Deploy build folder to gh-pages"

# Push the changes to the gh-pages branch
git push origin gh-pages --force
```

### Verify Deployment

After deployment, you can verify your site is live by checking the GitHub Pages settings in your repository's `Settings` and visiting `https://<username>.github.io/my-website/`.



## 2 Let me think 

