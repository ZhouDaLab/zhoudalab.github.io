# ZhouDa Lab Website

This is the website of our academic research group at Xiamen University.

This website is powered by Jekyll and some Bootstrap, Bootwatch. We tried to make it simple yet adaptable, so that it is easy for you to use it as a template. Plese feel free to copy and modify for your own purposes.  You don't have to link to us or mention us (but of course we appreciate it).

Go to *aboutwebsite.md*  to learn how to copy and modidy this page for your purpose. 

## 如何更新内容
如果是在github上更新，直接在网页上打开相应文件，点blame右边的按钮编辑，改好后点最下面的`Commit changes`即可。更新后打开网页链接 zhoudalab.github.io 按ctrl+F5刷新缓存后可以看到改动（有时可能有一些延迟）。  
### 1. 更新主页，招生说明和文章
- 主页为/_pages/home.md，  
- 招生说明为/_pages/openings.md,  
- 文章为/_pages/publications.md  
- 直接修改即可  
### 2. 更新课题组成员和课题组动态
- 课题组成员为/_data/students.yml
- 课题组动态为/_data/news.yml
- 复制其中一条然后修改内容，注意格式一致
### 3. 修改网页的header和footer
- 分别位于 /_includes/header.html 和 /_includes/footer.html
### 4. 修改主页右侧的 See all news 的链接
- /_includes/news.html 第9行链接
### 5. 其它文件夹介绍
- /downloads 用于存放文件，可以挂到网站上供下载
- /images 用于存放网站使用的图片
- /_data/buckup 存放了一些成员介绍的不同模本，有的带图有的不带图，可以替换/_data/students.yml，也可以不同的人用不同的模本，参考http://www.allanlab.org/team
