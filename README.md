# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

```sh
npm create vite@latest .
```

```
React
Javascript
```

```sh
npm install
npm run dev

npm install --save-dev prettier eslint eslint-plugin-react eslint-config-prettier eslint-plugin-jsx-a11y
npx eslint src
npx eslint src --fix
npx eslint src
npm pkg set scripts.lint="eslint src"
npm run lint
npm install --save-dev husky lint-staged

git init -b master
git add package.json
git commit -am "chore: Initial commit"

npm pkg set scripts.prepare="husky install"
npm run prepare
npx husky init
echo "npx lint-staged" > .husky/pre-commit

git add .
git commit -m "chore: Basic project setup"

npm install --save-dev @commitlint/cli @commitlint/config-conventional
echo "npx commitlint --edit ${1}" > .husky/commit-msg
npx husky add .husky/commit-msg 'npx commitlint --edit ${1}'

git add .
git commit -m "no type"
git commit -m "wrong: type"
git commit -m "chore: Configure commitlint"
```

```sh
docker run -it ubuntu:24.04 /bin/bash
uname -a
exit

docker run -d --name dbserver -p 27017:27017 --restart unless-stopped mongo:6.0.4
mongosh mongodb://localhost:27017/ch2
console.log("test")

db.users.insertOne({ username: 'dan', fullName: 'Daniel Bugl', age: 26 })
db.users.find()

db.users.insertMany([
  { username: 'jane', fullName: 'Jane Doe', age: 32 },
  { username: 'john', fullName: 'John Doe', age: 30 }
])

db.users.findOne({ username: 'jane' })
db.users.find({ fullName: 'Daniel Bugl' })
db.users.findOne({ _id: ObjectId('6405f062b0d06adeaeefc3bc') })
db.users.find({ age: { $gt: 30 } })
db.users.find().sort({ age: 1 })

# Updating documents
db.users.updateOne({ username: 'dan' }, { $set: { age: 27 } })
db.users.updateOne({ username: 'new' }, { $set: { fullName: 'New User' } })
db.users.updateOne({ username: 'new' }, { $set: { fullName: 'New User' } }, { upsert: true })

db.users.deleteOne({ username: 'new' })
```

**Accessing the database via VS Code**

1. Click on the MongoDB icon on the left sidebar
2. A new **MongoDB** tab will open up. In this tab, click on `Connect` in the `Connect with Connection String` box:
3. A popup should open at the top. In this popup, enter the following connection string to connect to your local database:

   ```
   mongodb://localhost:27017/
   ```

**Accessing the MongoDB database via Node.js**

```sh
npm install mongodb
node backend\mongodbweb.js
```

```sh
npm uninstall --save react react-dom
npm uninstall --save-dev vite @types/react @types/react-dom @vitejs/plugin-react eslint-plugin-jsx-a11y eslint-plugin-react

npm install mongoose
```

```sh
npm install --save-dev jest mongodb-memory-server
npm install express
npm install dotenv
npm install –save-dev nodemon
npm install body-parser
npm install cors
```
