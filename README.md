# PHP/Xdebug/Docker example

Debug PHP with Xdebug inside Docker. Tested with PhpStorm and VS Code.

## Usage

The Xdebug config happens in the `Dockerfile`. I recommend to look at it, escpeially the comments. The most important part is the `xdebug.remote_host` which has to be set to the Docker host.

 A sample `docker-compose.yml` comes along with it so you can get this up and running in one command: `docker-compose up --build -d`.

## VS Code configuration

Install the [felixfbecker.php-debug](https://marketplace.visualstudio.com/items?itemName=felixfbecker.php-debug) extension.

You can create a debug configuration by going to `Debug > Add Configuration... > PHP`, but I've included the `.vscode/launch.json` file in the repo, with the correct folder maping.

Add a breakpoint, and click on "Listen for XDebug" in the top left hand corner. Load your page, and you should get debugging information:

![](https://i.imgur.com/B8dnAj7.png)

## PhpStorm configuration

You should not have to configure anything since we use the default debug port etc.

Add a breakpoint and start listening for Xdebug in the top right hand corner:

![](https://i.imgur.com/05hPG89.png)

Load your page. PhpStorm will prompt you to add a "server" with a folder mapping:

![](https://i.imgur.com/Z846Zoh.png)

And then magic happens:

![](https://i.imgur.com/yUnpilx.png)

Enjoy 👋
