# - simple picture array maker -

creates a montage / array of pictures which will be unified, squared and optionally cropped.
it supports an adjustable gap between pictures, layout and rounded corners.

## dependencies

- bash
- GraphicsMagick

## usage

run `./photosh <DIR>` or move it into a `$PATH` directory of your choice to run it from anywhere.

all command flags are optional, since default values have been implemented.

```sh
$ ./photosh -h
```
```
>
simple picture array maker
Usage: ./photosh [-s VALUE] [-k VALUE] [-b VALUE] [-c VALUE] [-r VALUE] [-t] [-h] [DIRECTORY]
  if DIRECTORY is omitted, the current one will be used
  default values are in [...]

  -s   maximum tilesize in px  [200]
  -k   corner radius in px  [0]
  -b   border around each tile in px  [10]
        (equates to half the gap between each tile)
  -c   amount of pictures horizontally (columns)  [3]
  -r   amount of pictures vertically (rows)  [3]
  -t   crop / trim non-squared pictures  [no]
  -h   show this help
```

with the added html UI you can locally preview all options.

it also generates a commandline output accordingly to paste it into a terminal.

### note:

make sure that your input directory includes *only* images.
dot-files, html, markdown and files w/o filetype extension are excluded: `.*`, `*.md`,`*.html` and `!*.*`
since Graphics Magick supports a wide array of image formats, there are no other exclusion of filetypes hardcoded.


## todo

- [x] add support for multiple directories
- [ ] choose different background colors
- [x] add simple html UI for previewing and generating the corresponding commandline
