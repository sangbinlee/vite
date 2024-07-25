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

# vi tip - 자동정렬

    1. shift + v
    2. 방향키로 라인 선택
    3. \=
    4. 자동정렬 완료

# preview setting

    server {
        server_name vite.sodi9.store;
        root /var/www/vite;
        index index.html;

        # location / {
        #        try_files $uri $uri/ =404;
        #}

        listen [::]:443 ssl ipv6only=on; # managed by Certbot
        listen 443 ssl; # managed by Certbot
        ssl_certificate /etc/letsencrypt/live/vite.sodi9.store/fullchain.pem; # managed by Certbot
        ssl_certificate_key /etc/letsencrypt/live/vite.sodi9.store/privkey.pem; # managed by Certbot
        include /etc/letsencrypt/options-ssl-nginx.conf; # managed by Certbot
        ssl_dhparam /etc/letsencrypt/ssl-dhparams.pem; # managed by Certbot

        location / {

                proxy_set_header        Host $host;
                proxy_set_header        X-Real-IP $remote_addr;
                proxy_set_header        X-Forwarded-For $proxy_add_x_forwarded_for;
                proxy_set_header        X-Forwarded-Proto $scheme;

                # Fix the "It appears that your reverse proxy set up is broken" error.
                proxy_pass          http://127.0.0.1:3004;
                proxy_read_timeout  90;
        }
    }

    server {
            if ($host = vite.sodi9.store) {
                    return 301 https://$host$request_uri;
            } # managed by Certbot


            listen 80;
            listen [::]:80;
            server_name vite.sodi9.store;
            return 301 https://$host$request_uri;

    }

# restart nginx

    sudo systemctl restart nginx
