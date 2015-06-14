lambda-kollektiv.github.io
=================
Our team blog.

## INSTALLATION
`Ruby >= 2.0.0` is required as jekyll is used on gh-pages. Check version:

```
ruby --version
```

If not installed:

```
sudo apt-get install ruby
```

Install `bundler` for easier ruby lib management configured in `Gemfile`:
```
sudo gem install bundler
```

Now run the server:

```
bundle exec jekyll server
```

and for drafts run 
```
bundle exec jekyll server --drafts
```
