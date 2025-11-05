# Bug Report: Missing Development Dependencies

## Description
When trying to run the development server using `npm run dev`, the following error occurs:
```
nodemon: command not found
```

## Expected Behavior
Running `npm run dev` should start the development server with nodemon for hot-reloading.

## Steps to Reproduce
1. Clone the repository
2. Run `npm install`
3. Run `npm run dev`

## Solution
1. Install nodemon as a development dependency:
   ```bash
   npm install --save-dev nodemon
   ```
2. Verify the installation by checking `package.json`:
   ```json
   "devDependencies": {
     "nodemon": "^2.0.4"
   }
   ```
3. Try running `npm run dev` again

## Additional Notes
- Make sure you have the latest version of Node.js and npm installed
- If the issue persists, try deleting `node_modules` and `package-lock.json` then run `npm install` again

---
*This is an automated issue template. If you're experiencing this issue, please follow the solution steps above.*
