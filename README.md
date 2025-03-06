Contains noto emoji shredded using [ttx](https://fonttools.readthedocs.io/en/latest/_modules/fontTools/ttx.html):

```shell
# Grab an emoji file, such as v2.047 from https://github.com/googlefonts/noto-emoji/blob/main/fonts/NotoColorEmoji.ttf
# We'll assume it's in ~/Downloads/NotoColorEmoji.ttf

# Setup a venv if that's how you like to live
$ python3 -m venv venv
$ source venv/bin/activate

# Install FontTools
$ pip install fonttools

# Make a directory for the torn apart font
$ ttx -o - -t name ~/Downloads/NotoColorEmoji.ttf
# ^ suggests this is v2.047
$ mkdir v2.047
$ cd v2.047
$ cp ~/Downloads/NotoColorEmoji.ttf .

# TTX with bitmaps dumped to individual files
$ ttx -z extfile NotoColorEmoji.ttf
```
