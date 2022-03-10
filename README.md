# [docs.pan-training.eu](https://docs.pan-training.eu/)
Docs for [PaN e-Learning](https://e-learning.pan-training.eu/)

## Add/Edit a page 

To include a new page add a markdown file to the [docs](https://github.com/pan-training/pan-training.github.io/tree/gh-pages/docs) folder. Here you can also edit the existing pages. 

Ensure you include the permalink, classes and title in the yaml preamble (see an existing page for an example). 

### Add new page to side naviation 

To inlcude your new page in the side navigation add the title and path to the [_data/navigation.yml](https://github.com/pan-training/pan-training.github.io/blob/gh-pages/_data/navigation.yml) file.

The site is currently set such that every page has the same side navigation on the left. Currently none of the pages a toc on the right, but this is a possibility if a page is very long. 

### Including figure/images 

You can upload your images to [assests/img](https://github.com/pan-training/pan-training.github.io/tree/gh-pages/assets/img). This may get a little full and need a better organisation. 

## The site

The site uses the minimal mistakes jekyll theme  
https://github.com/mmistakes/minimal-mistakes

A few changes have been applied
- smaller font size for the main body of test
- larger font size for the side navigation
- custom notice style 

favicons were generated using https://realfavicongenerator.net/

###  Run locally 

Install Ruby.
```
sudo apt-get install ruby-full build-essential zlib1g-dev
```
Add environment variables to ~/.bashrc 
```
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```
Install jekyll and bundler
```
gem install bundler jekyll
```
Clone repo
```
git clone https://github.com/pan-training/pan-training.github.io
cd pan-training.github.io
```
Run locally
```
bundle exec jekyll serve
```

