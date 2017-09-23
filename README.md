<p align="center">
  <img src="https://s3.amazonaws.com/ohmyzsh/oh-my-zsh-logo.png" alt="Oh My Zsh">
</p>

Oh My Zsh 是由社区驱动的一个开源的框架, 用于管理你的[zsh](http://www.zsh.org/) 配置.

听上去有点无聊. 让我们再来试一下.

__Oh My Zsh 虽然不能让你提升10倍的效率...但你或许会感觉像是那样.__

一旦安装完成, 你的终端shell将会成为小镇上的谈资 _或者让你的钱回来!_ 伴随着按键提示, 你将获得成百上千高级的给力的插件以及炫酷的主题. 甚至在咖啡馆的陌生人会找上你,并和你说, _"这太屌了!你是某种天才?"_

最后, 你将会得到某些你所应得的关注...或者你也可以使用你所节省的时间来更频繁的使用牙线(美国人的幽默?).

想知道更多? 看一下这个网站 [ohmyz.sh](http://ohmyz.sh) 并且在推特上关注 [@ohmyzsh](https://twitter.com/ohmyzsh) .

## 让我们开始吧

### 准备工作

__温馨提示:__ _Oh My Zsh 在苹果和Linux上工作的最好._

* 类unix操作系统 (苹果或linux)
* 需要先安装上 [Zsh](http://www.zsh.org)  (v4.3.9 or more recent). 如果没有预先安装 (可以用这条命令来确认一下`zsh --version` ), 那就看一下这里: [Installing ZSH](https://github.com/robbyrussell/oh-my-zsh/wiki/Installing-ZSH)
* 也需要安装 `curl` 或 `wget` 
* 还有 `git`

### 基本安装

Oh My Zsh is 通过下面的命令来安装. 你可以选择用 `curl` 或者 `wget`来下载脚本,并执行安装.

#### 通过 curl

```shell
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

#### 通过 wget

```shell
sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```

## 使用 Oh My Zsh

### 插件

Oh My Zsh 通过加载各种插件来提供高级功能. 你可以看一下 [plugins](https://github.com/robbyrussell/oh-my-zsh/tree/master/plugins) 目录,或者 [wiki](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins) 来了解现在有那些可以用的插件.

#### 启用 Plugins
一旦你找到一个想要的插件, 你需要在 `.zshrc` 文件中启用他们. 你可以在 `$HOME` 目录下找到`.zshrc`. 用你最爱的文本编辑器打开它,然后你会看到有一个地方列出了所有你想要加载的插件.

例如, 这一行最开始像这样:

```shell
plugins=(git bundler osx rake ruby)
```

#### 使用插件

绝大多数的插件 (我们正在进行这项工作) 都包含一个 __README__, 你可以从这里了解如何使用它.

### 主题

我们承认, 在早期的 Oh My Zsh 世界, 我们在主题上获得了很大的乐趣. 我们现在有超过一百个主题, 它们绝大多数都有[截图](https://wiki.github.com/robbyrussell/oh-my-zsh/themes) 放在在wiki上. 快去看看吧!

#### 选择一个主题

_Robby 的主题是默认的. It's not the fanciest one. It's not the simplest one. 它只是最适合的一个 (对Robby来说)._

一旦你找到你想用的主题, 你需要去编辑 `~/.zshrc` 文件. 你会看到一个环境变量 (所有字母都大写) 看上去像这样:

```shell
ZSH_THEME="robbyrussell"
```

如果要换成其他的主题, 只需要简单的将值修改为你像要的主题的名字. 例如:

```shell
ZSH_THEME="agnoster" # (this is one of the fancy ones)
# you might need to install a special Powerline font on your console's host for this to work
# see https://github.com/robbyrussell/oh-my-zsh/wiki/Themes#agnoster
```
打开一个新的终端窗口, 你的界面就会类似变成这样:

![Agnoster theme](https://cloud.githubusercontent.com/assets/2618447/6316862/70f58fb6-ba03-11e4-82c9-c083bf9a6574.png)

以免你找不到你所需要的主题, 请看一下这个wiki[更多的主题](https://github.com/robbyrussell/oh-my-zsh/wiki/External-themes).

如果你想尝鲜, 你可以让计算机随机的选择一个主题, 这样在你每次打开终端窗口都会有新的发现.

```shell
ZSH_THEME="random" # (...please let it be pie... please be some pie..)
```


## 高级篇

If you're the type that likes to get their hands dirty, these sections might resonate.

### Advanced Installation

一些用户可能想修改默认的路径,或是手动安装 Oh My Zsh.

#### 自定义路径

默认的位置是 `~/.oh-my-zsh` (隐藏在你的家目录, _通常按Ctrl+h可以在文件图形文件管理器中看到隐藏文件, 用`ls -a` 可以在终端看到--译者注_)

如果你想改变安装目录, 你可以修改环境变量 `ZSH` , 通过在执行安装命令前执行 `export ZSH=/your/path`, 或者通过下面这条命令来进行设置(请注意ZSH的值):

```shell
export ZSH="$HOME/.dotfiles/oh-my-zsh"; sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

#### 手动安装

##### 1. 克隆软件仓库:

```shell
git clone git://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh
```

##### 2. *可选*, 备份你的 `~/.zshrc` 文件:

```shell
cp ~/.zshrc ~/.zshrc.orig
```

##### 3. 创建一个新的

你可以通过复制我们预先给你准备好的文件来创建一个新的zsh配置文件.
```shell
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
```

##### 4. 修改默认shell

```shell
chsh -s /bin/zsh
```

##### 5. 初始化你新的zsh配置

一旦你打开一个终端窗口, 它应该会自动加载zsh的配置.

### 安装问题

如果你在安装过程中出现了问题, 这里有几个通用的方法可以试一下.

* 如果你无法找到在使用oh-my-zsh之前使用的命令, 你 _或许_ 需要去修改 `~/.zshrc` 文件中 的`PATH` 环境变量.
* 如果你手动安装或者修改了安装位置, 检查一下`~/.zshrc` 文件中的 `ZSH`环境变量.
### 自定义插件和属性

如果你想覆盖任何默认行为, 只需要添加新的文件
If you want to override any of the default behaviors, just add a new file (ending in `.zsh`) in the `custom/` directory.

If you have many functions that go well together, you can put them as a `XYZ.plugin.zsh` file in the `custom/plugins/` directory and then enable this plugin.

If you would like to override the functionality of a plugin distributed with Oh My Zsh, create a plugin of the same name in the `custom/plugins/` directory and it will be loaded instead of the one in `plugins/`.

## Getting Updates

By default, you will be prompted to check for upgrades every few weeks. If you would like `oh-my-zsh` to automatically upgrade itself without prompting you, set the following in your `~/.zshrc`:

```shell
DISABLE_UPDATE_PROMPT=true
```

To disable automatic upgrades, set the following in your `~/.zshrc`:

```shell
DISABLE_AUTO_UPDATE=true
```

### Manual Updates

If you'd like to upgrade at any point in time (maybe someone just released a new plugin and you don't want to wait a week?) you just need to run:

```shell
upgrade_oh_my_zsh
```

Magic!

## Uninstalling Oh My Zsh

Oh My Zsh isn't for everyone. We'll miss you, but we want to make this an easy breakup.

If you want to uninstall `oh-my-zsh`, just run `uninstall_oh_my_zsh` from the command-line. It will remove itself and revert your previous `bash` or `zsh` configuration.

## Contributing

I'm far from being a [Zsh](http://www.zsh.org/) expert and suspect there are many ways to improve – if you have ideas on how to make the configuration easier to maintain (and faster), don't hesitate to fork and send pull requests!

We also need people to test out pull-requests. So take a look through [the open issues](https://github.com/robbyrussell/oh-my-zsh/issues) and help where you can.

### Do NOT send us themes

We have (more than) enough themes for the time being. Please add your theme to the [external themes](https://github.com/robbyrussell/oh-my-zsh/wiki/External-themes) wiki page.

## Contributors

Oh My Zsh has a vibrant community of happy users and delightful contributors. Without all the time and help from our contributors, it wouldn't be so awesome.

Thank you so much!

## Follow Us

We're on the social media.

* [@ohmyzsh](https://twitter.com/ohmyzsh) on Twitter. You should follow it.
* [Oh My Zsh](https://www.facebook.com/Oh-My-Zsh-296616263819290/) on Facebook.

## Merchandise

We have [stickers](http://shop.planetargon.com/products/ohmyzsh-stickers-set-of-3-stickers) and [shirts](http://shop.planetargon.com/products/ohmyzsh-t-shirts) for you to show off your love of Oh My Zsh. Again, this will help you become the talk of the town!

## License

Oh My Zsh is released under the [MIT license](LICENSE.txt).

## About Planet Argon

![Planet Argon](http://pa-github-assets.s3.amazonaws.com/PARGON_logo_digital_COL-small.jpg)

Oh My Zsh was started by the team at [Planet Argon](https://www.planetargon.com/?utm_source=github), a [Ruby on Rails development agency](https://www.planetargon.com/skills/ruby-on-rails-development?utm_source=github).

## 翻译
中文翻译由四级都没过的空耳大师ruinb0w完成
