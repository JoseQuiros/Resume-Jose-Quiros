# GitHub Pages Deployment

## Repository Setup on GitHub

### 1. Configure GitHub Pages
1. Go to your repository on GitHub
2. Navigate to **Settings** → **Pages**
3. Under **Source**, select **GitHub Actions**

### 2. Push the changes
```bash
git add .
git commit -m "Add GitHub Pages deployment workflow"
git push origin main
```

### 3. Deployment will run automatically
- Every time you push to the `main` branch
- You can also run it manually from the **Actions** tab

## Access URLs
- **Local development**: http://localhost:5173/
- **GitHub Pages**: https://[your-username].github.io/Resume-Jose-Quiros/

## Useful commands

```bash
# Start development server
npm run dev

# Create production build
npm run build

# Preview production build
npm run preview
```

## Workflow structure

The `.github/workflows/deploy.yml` file contains:
- ✅ Node.js 18 setup
- ✅ Dependencies installation
- ✅ Project build
- ✅ Automatic GitHub Pages deployment
- ✅ Correct permissions configuration

## Important notes
- The workflow runs on Ubuntu
- Uses official GitHub Actions for Pages
- The project builds to the `dist` directory
- Vite configuration includes the correct `base` for GitHub Pages 