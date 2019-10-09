# fast-catch
短小精悍的前端缓存工具，防止内存‘侧漏’

## 简介

## 安装下载


## 快速使用

- [使用文档](./doc/use/part1/README.md)
- [二次开发文档](./doc/use/part2/README.md)

## 交流 & 提问

## 关于作者

- 个人主页

- 收款二维码

## 自己创建、维护一个项目
1. 在git 上创建一个库 （创建时，add a license ： mit License ）
2.  ssh key 连接电脑和github 服务器的一把钥匙，只有添加成功了才能把本地的代码提交到github服务器。
3.终端运行 ssh-keygen 即可生成ssh key ,然后运行 pbcopy < ~/.ssh/id_rsa.pub 即可拷贝下来，等待粘贴。
4. 在github个人中心的设置界面，找到SSH and GPS keys 菜单栏，点击右侧‘new ssh key’ 按钮即可添加ssh key,把刚才的内容粘贴过来就添加上了。
5. 修改用户名： git config user.name 'new name'
修改邮箱：git config user.email 'fast-catch@gemail.com'

6. npm init 创建一个项目 
7. npm i babel-core babel-loader babel-polyfill babel-preset-es2015 babel-preset-latest webpack webpack-cli --save-dev
8. 项目根目录下创建 .babelrc 文件，内容如
{
"presets": ["es2015", "latest"],
"plugins": []
}
9. 根目录下创建webpack.config.js 文件
module.exports = {
  entry: './src/index.js',
  output: {
    path: __dirname,
    filename: './release/bundle.js'
  },
  module: {
    rules: [{
      test: /\.js?$/,
      exclude: /(node_modules)/,
      loader: 'babel-loader'
    }]
  }
}
10. 修改package.json文件的script 对象，"dev": "webpack --mode development",
    "build": "webpack --mode production"
11. npm install http-server -g
package.json文件修改script 对象添加： example : "http-server -p 8880" // example 为文件夹名称  8880 为端口号
12. npm run dev
13. 浏览器输入 localhost:8880/example/test.html
14. 写需求文档： npm install gitbook -g
15. 根目录下创建SUMMARY.md 
    内容：
* [Introduction](README.md)
* [Part I](doc/use/part1/README.md)
    * [Writing is nice](doc/use/part1/writing.md)
    * [GitBook is nice](doc/use/part1/gitbook.md)
* [Part II](doc/use/part2/README.md)
    * [We love feedback](doc/use/part2/feedback_please.md)
    * [Better tools for authors](doc/use/part2/better_tools.md)
16. 创建doc目录： gitbook init 
    然后完成文档
17. gitbook build
18. 