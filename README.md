[Guan Blog](http://guanyugangstar.github.io)
================================

> I never expected this to become popular.


[User Manual 👉](_doc/Manual.md)
--------------------------------------------------

### Getting Started

1. You will need [Ruby](https://www.ruby-lang.org/en/) and [Bundler](https://bundler.io/) to use [Jekyll](https://jekyllrb.com/). Following [Using Jekyll with Bundler](https://jekyllrb.com/tutorials/using-jekyll-with-bundler/) to fullfill the enviromental requirement.

2. Installed dependencies in the `Gemfile`:

```sh
$ bundle install 
```

3. Serve the website (`localhost:4000` by default):

```sh
$ bundle exec jekyll serve  # alternatively, npm start
```

### Windows Deployment

If you are using Windows, follow these steps to set up and run the blog:

1. **Install Ruby with DevKit**:
   - Download and install the latest Ruby+Devkit from [RubyInstaller for Windows](https://rubyinstaller.org/)
   - During installation, make sure to check "Add Ruby executables to your PATH"
   - When prompted, choose to install MSYS2 and development toolchain

2. **Install Bundler**:
   ```sh
   gem install bundler
   ```

3. **Install Dependencies**:
   Navigate to your project directory and run:
   ```sh
   bundle install
   ```

4. **Configure Environment Variables**:
   - Copy `start.bat.example` to `start.bat`
   - Edit `start.bat` and replace the placeholder values with your actual LeanCloud App ID and App Key

5. **Run the Blog**:
   You can start the blog in two ways:
   - Using the start script (recommended):
     ```sh
     start.bat
     ```
   - Using Jekyll directly:
     ```sh
     bundle exec jekyll serve
     ```
   - Using npm script (requires Node.js):
     ```sh
     npm start
     ```

6. **Access the Blog**:
   Open your browser and go to `http://localhost:4000` to view your blog.

### Development (Build From Source)

To modify the theme, you will need [Grunt](https://gruntjs.com/). There are numbers of tasks you can find in the `Gruntfile.js`, includes minifing JavaScript, compiling `.less` to `.css`, adding banners to keep the Apache 2.0 license intact, watching for changes, etc. 

Yes, they were inherited and are extremely old-fashioned. There is no modularization and transpilation, etc.

Critical Jekyll-related code are located in `_include/` and `_layouts/`. Most of them are [Liquid](https://github.com/Shopify/liquid/wiki) templates.

This theme uses the default code syntax highlighter of jekyll, [Rouge](http://rouge.jneen.net/), which is compatible with Pygments theme so just pick any pygments theme css (e.g. from [here](http://jwarby.github.io/jekyll-pygments-themes/languages/javascript.html) and replace the content of `highlight.less`.


### Interesting to know more? Checkout the [full user manual](_doc/Manual.md)!


Other Resources
---------------

Ports
- [**Hexo**](https://github.com/Kaijun/hexo-theme-huxblog) by @kaijun
- [**React-SSR**](https://github.com/LucasIcarus/huxpro.github.io/tree/ssr) by @LucasIcarus

[Starter/Boilerplate](https://github.com/guanyugangstar/guanblog-boilerplate)
- Out of date. Helps wanted for updating it on par with the main repo

Translation
- [🇨🇳  中文文档（有点过时）](https://github.com/guanyugangstar/guanyugangstar.github.io/blob/master/_doc/README.zh.md)


License
-------

Apache License 2.0.
Copyright (c) 2015-present guanyugangstar

Guan Blog is derived from [Clean Blog Jekyll Theme (MIT License)](https://github.com/BlackrockDigital/startbootstrap-clean-blog-jekyll/)
Copyright (c) 2013-2016 Blackrock Digital LLC.
