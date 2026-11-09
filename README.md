# heroku-buildpack-rsvg
rsvg ported to heroku

Using this buildpack you can call on heroku:

    $ rsvg-convert -o my_image.pdf my_image.svg
    
There is nothing more or less.

## Supported stacks

The binary is chosen by `$STACK` from `rsvg/<stack>/rsvg-convert`:

- `heroku-22`
- `heroku-24`: `rsvg-convert` from Ubuntu noble's `librsvg2-bin_2.58.0+dfsg-1ubuntu0.1_amd64.deb`

The build fails on any other stack, and also fails if the binary can't convert `rsvg/test.svg`.
