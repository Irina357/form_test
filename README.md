# Проект Form.
Этот проект реализован с использованием следующих технологий:
1. vue.js
   1. components
   1. props
   1. пользовательские события $emit
   1. MaskedInput
1. Css
   1. SASS
##  Как это работает.
После заполнения формы нажмите кнопку Submit. В случае корректного заполнения формы возникнет сообщение о регистрации, с которого можно вернуться для редактирования 
формы или перейти к дальнейшим действиям.
### Настройка проекта
Для запуска проекта на машине разработчика используйте в консоли следующие команды:
* npm install
* npm run serve
### Для публикации проекта на GitHab Pages:
1. В файле vue.config.je укажите название вашего репозитория на GitHab:
`module.exports = {
    publicPath: process.env.NODE_ENV === 'production' ? '/YOUR_REPO_NAME/' : '/'
}`
1. соберите проект, введя в консоли команду:
npm run build
3. После создания папки Dist, в файле deploy.sh также укажите название вашего репозитория на GitHab:
```
   set -e

npm run build

cd dist

git init
git add -A
git commit -m 'deploy'

git push -f git@github.com:YOUR_USER_NAME/REPOSITORY_NAME.git master:gh-pages

cd -
```

#### Посмотреть данный проект вы можете на [GitHab Pages](https://irina357.github.io/form_test/).
