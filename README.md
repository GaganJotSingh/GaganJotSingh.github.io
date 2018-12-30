# Build and run on Windows 7
* Install ruby using RubyInstaller and "jekyll" bundle from the link https://jekyllrb.com/docs/windows/
* Clone the repo in local system
* Go to the repo path in cmd and run below command: ´bundle update && bundle install´
This will update the gems required by your site using the files Gemfile and Gemfile.lock
* Host site locally by running the file "serve.bat" in cmd as: ´serve.bat´ OR ´.\serve.bat´
  - Use Windows CMD or PowerShell for running this, as Git shell doesn't run this correctly.

# Build and run on Linux
* Get started here: https://jekyllrb.com/docs/quickstart/
* Clone the repo in local system
* Go to the repo path in terminal and run below command: ´bundle update && bundle install´
This will update the gems required by your site using the files Gemfile and Gemfile.lock
* Host site locally by running the file "serve.sh" in terminal as: ´serve.sh´

# Common
* The site is hosted by default at http://localhost:4000 until there are some changes in the running command via the params.

# Initiate Jekyll site
* To create a new jekyll site follow: https://jekyllrb.com/docs/quickstart/#options-for-creating-a-new-site-with-jekyll
* E.g. If you already have a repo cloned to local which is not yet a jekyll site then to make that repo into a site, go to that repo from cmd and run this command:
´jekyll new . --force´
This will also run ´bundle install´ which installs the gems required by the site.
