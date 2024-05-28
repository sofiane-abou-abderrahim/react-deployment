# Deploying React Apps

## From Development To Production

- Deployment Steps & Pitfalls
  1. Test Code: Manually & with automated tests
  2. Optimize Code: Optimize user experience & performance
     1. Lazy Loading: Load code only when it's needed
     2. Having to load all the code initially will slow down that initial page load
  3. Build App: Run build process to parse, transform & optimize code
  4. Upload App: Upload production code to hosting server
  5. Configure Server: Ensure app is served securely & as intended
- Server-side Routing vs Client-side Routing

# Steps

## 0. Project Setup

1. run `npm install`
2. run `npm start`
3. create a `README.md` file
4. create a `.gitignore` file

## 1. Adding Lazy Loading

1. in `App.js`, in order to load the `BlogPage` lazily, remove the `import` of the `BlogPage` & the `PostPage`
2. load the `loader`lazily by using the `import()` function
3. load the `BlogPage` & `PostPage` components lazily
4. use the `lazy()` fonction imported from `react`
5. wrap the `<BlogPage>` & `<PostPage>` components with the `<Suspense>` component imported from `react`

## 2. Building the Code For Production

1. in the terminal, execute `npm run build`
2. a `build` folder is created & ready to be rendered

## 3. Deployment Example

1. in Firebase Hosting, create a new project named `react-deployment-demo` for example
2. in your terminal, run
   1. `npm install -g firebase-tools`
   2. `firebase login`
   3. `firebase init`
   4. `firebase deploy`
