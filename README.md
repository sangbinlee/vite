# Vue 3 + Vite

This template should help get you started developing with Vue 3 in Vite. The template uses Vue 3 `<script setup>` SFCs, check out the [script setup docs](https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup) to learn more.

Learn more about IDE Support for Vue in the [Vue Docs Scaling up Guide](https://vuejs.org/guide/scaling-up/tooling.html#ide-support).
"# vite" 




# set up

    C:\Users\sangb\vite>npm create vite@latest vite-vue-app-1 -- --template vue

    > npx
    > create-vite vite-vue-app-1 --template vue


    Scaffolding project in C:\Users\sangb\vite\vite-vue-app-1...

    Done. Now run:

    cd vite-vue-app-1
    npm install
    npm run dev


    C:\Users\sangb\vite>  cd vite-vue-app-1

    C:\Users\sangb\vite\vite-vue-app-1>  npm install

    added 27 packages, and audited 28 packages in 11s

    4 packages are looking for funding
    run `npm fund` for details

    found 0 vulnerabilities

    C:\Users\sangb\vite\vite-vue-app-1>  npm run dev

    > vite-vue-app-1@0.0.0 dev
    > vite


    VITE v5.3.5  ready in 2056 ms

    ➜  Local:   http://localhost:5173/
    ➜  Network: use --host to expose
    ➜  press h + enter to show help
    일괄 작업을 끝내시겠습니까 (Y/N)?
    ^C
    C:\Users\sangb\vite\vite-vue-app-1>code .


    C:\Users\sangb\vite\vite-vue-app-1>echo "# vite" >> README.md

    C:\Users\sangb\vite\vite-vue-app-1>git init
    Initialized empty Git repository in C:/Users/sangb/vite/vite-vue-app-1/.git/

    C:\Users\sangb\vite\vite-vue-app-1>git add README.md
    warning: in the working copy of 'README.md', LF will be replaced by CRLF the next time Git touches it

    C:\Users\sangb\vite\vite-vue-app-1>git commit -m "first commit"
    [master (root-commit) bf8edb0] first commit
    1 file changed, 6 insertions(+)
    create mode 100644 README.md

    C:\Users\sangb\vite\vite-vue-app-1>git branch -M main

    C:\Users\sangb\vite\vite-vue-app-1>git remote add origin https://github.com/sangbinlee/vite.git

    C:\Users\sangb\vite\vite-vue-app-1>git push -u origin main
    Enumerating objects: 3, done.
    Counting objects: 100% (3/3), done.
    Delta compression using up to 20 threads
    Compressing objects: 100% (2/2), done.
    Writing objects: 100% (3/3), 454 bytes | 454.00 KiB/s, done.
    Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
    To https://github.com/sangbinlee/vite.git
    * [new branch]      main -> main
    branch 'main' set up to track 'origin/main'.