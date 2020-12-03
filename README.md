<div align="center">

# translate

A chinese--english translate tool in your command line.

</div>

## Install

```bash
$ npm install @yuezheng2006/translate -g
```

## Usage

```bash
$ translate word
```

For short:

```bash
$ trans word
```

Translation data is fetched from [金山词霸](http://iciba.com) and [有道翻译](http://fanyi.youdao.com), and only support translation between Chinese and English.

In Mac/Linux bash, words will be pronounced by `say` command.

Translate one word.

```bash
$ trans awesome
```

```js

 awesome  [ ˈɔːsəm ]  ~  有道翻译

 - adj. 令人敬畏的；使人畏惧的；可怕的；极好的

 1. Awesome
    真了不起,傲森
 2. Totally Awesome
    绝妙青春,绝对震憾
 3. Agent Awesome
    完美特工

  --------

⠸  awesome  英[ ˈɔ:səm ]  美[ ˈɔsəm ]  ~  金山翻译

 - adj. 令人敬畏的；使人畏惧的；可怕的；极好的；

 1. Many thanks to all the awesome developers that wrote such an awesome threads.
    所有的写了这样一真棒线程真棒开发商非常感谢.
 2. Brah: Thanks a bunch . are awesome to teach me so much.
    布莱: 多谢, 你真好,教我这么多.
 3. The video disk stores an awesome amount of information.
    电视唱片贮存着数量惊人的信息.
 4. Feel the awesome might of the Feron horde.
    在战斗中感受它吧.
 5. Awesome ! I for one welcome our new overlords ---- AcoRS.
    哦,不错,欢迎我们的新霸主.

  --------


```

More words.

```bash
$ trans make love
```

Support Chinese

```bash
$ trans 和谐
```

## Configuration

A configuration file can be put into `~/.transrc`, in the user's home directory

Use subcommand `trans config [options]`

Example:

```bash
# Turn off the pronunciation
$ trans config --no-say
# or
$ trans config -S

# Disable the dictionaryapi
$ trans config --no-dictionaryapi
# or
$ trans config -D
```

A sample ~/.transrc file:

```json
{
  "iciba": false,
  "youdao": true,
  "say": false,
  "color": true
}
```

## Error: spawn festival ENOENT

Try this workaround from [say.js](https://github.com/Marak/say.js#linux-notes) in Linux.

```bash
sudo apt-get install festival festvox-kallpc16k
```
