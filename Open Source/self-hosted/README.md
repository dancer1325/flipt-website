* Flipt
  * == single binary / can run on host
    * Linux (x86-64 & ARM64) or
    * macOS (x86-64 & ARM64)
  * ways to install it
    * binary
      * `curl -fsSL https://get.flipt.io/install | sh`
        * install in '/usr/local/bin/flipt'
      * ->
        * `flipt [--config OPTIONAL_PATH_TO_YOUR_CONFIG]`
          * paths checked by default
            * '{{ USER_CONFIG_DIR }}/flipt/config.yml'
            * '/etc/flipt/config/default.yml'
    * docker
      * check '/docker'
    * kubernetes / helm
      * check '/kubernetes'
    * homebrew
      * `brew install flipt-io/brew/flipt`
      * -> 
        * run as a service -- `brew services start flipt` OR `flipt`
        * managed by [homebrew services](https://github.com/Homebrew/homebrew-services)