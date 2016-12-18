# Aget - Asynchronous Downloader

Aget is an asynchronous downloader operated in command-line, running on Python > 3.5.

It supports HTTP(S), using [mugen](https://github.com/PeterDing/mugen) request library.

Aget continues downloading a partially downloaded file as default.

### Installion

```shell
$ pip3 install aget
```

### Usage

```shell
aget https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png

# get an output name
aget https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png -o 'google.png'

# set headers
aget https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png -H "User-Agent: Mozilla/5.0" -H "Accept-Encoding: gzip"

# set concurrency
aget https://cdn.kernel.org/pub/linux/kernel/v4.x/linux-4.9.tar.xz -s 10

# set request range size
aget https://cdn.kernel.org/pub/linux/kernel/v4.x/linux-4.9.tar.xz -k 1M
```

### Arguments

```shell
-o OUT, --out OUT             # output path
-H HEADER, --header HEADER    # request header
-X METHOD, --method METHOD    # request method
-d DATA, --data DATA          # request data
-t TIMEOUT, --timeout TIMEOUT # timeout
-s CONCURRENCY, --concurrency CONCURRENCY   # concurrency
-k CHUCK_SIZE, --chuck_size CHUCK_SIZE      # request range size
```

