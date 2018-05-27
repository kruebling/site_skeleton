Hi James. I wrote really good instructions for you.

1.  install command-line tools (probably hopefully already have)

```
xcode-select --install
```

2. Install Brew (possibly maybe already have)

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

3. Check brew, if it returns anything other than "Your stystem is ready to brew" you'll have to troubleshoot

```
brew doctor
```

4. Download Ruby with Ruby Version Manager (and half the internet)

```
curl -L https://get.rvm.io | bash -s stable --auto-dotfiles --autolibs=enable --ruby
```

5. Check RVM, if it returns anything other than "rvm is a function" you'll have to do more troubleshooting and reach for a beer.

```
type rvm | head -1
```

6. Check versions of both RVM and Ruby

```
rvm -v
```

this should be rvm 1.26.10 or higher

```
ruby -v
```

this should be ruby 2.2.0 or higher, it should also be at least 2.3.3 for our purposes.

if you get `dyld: Library not loaded: /usr/local/lib/libgmp.10.dyli` you'll have to do more troubleshooting and possibly give up at this point.

7. Get bundler and jekyll. This is likes Rubys version of npm and jekyll is the ruby wrapper for our static site.
```
gem install bundler jekyll

```

8. Clone this repo.
```
git clone https://github.com/kruebling/site_skeleton.git
```

9. Trasnfer your potato ridden ancestry into said repo

```
cd site_skeleton
```

10. Install Deps

```
bundle install
```

11. View a current totally blank homepage

```
bundle exec jekyll serve
```

love,
-Keegan