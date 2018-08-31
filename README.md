## Getting Started

1. Install [Homebrew](https://brew.sh/):

    ```sh
    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    ```

2. Install OpenSSL libraries:

    ```sh
    brew install openssl
    ```

3. Install RVM and Ruby:

    ```sh
    curl -sSL https://get.rvm.io | bash -s stable
    # In a new session (restart your terminal or open new tab):
    rvm install 2.5.1 --default --with-openssl-dir=`brew --prefix openssl`
    ```

4. Set up RVM gemset:

    ```sh
    rvm gemset create cool_app
    rvm use 2.5.1@cool_app
    gem update --system
    gem update bundler
    gem install nokogiri -- --use-system-libraries=true --with-xml2-include=`xcrun --show-sdk-path`/usr/include/libxml2
    ```
