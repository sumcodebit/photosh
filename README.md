# - simple picture array maker -

creates a montage / array of pictures which will be unified, squared and optionally cropped.
it supports an adjustable gap between pictures, layout and rounded corners.

## dependencies

- bash
- Graphics Magick

## usage

run `./photosh <DIR>` or move it into a `$PATH` directory of your choice to run it from anywhere.

all command flags are optional, since default values have been implemented.

```sh
$ ./photosh -h
```
```
>
simple picture array maker
Usage: $0 [-s VALUE] [-k VALUE] [-b VALUE] [-c VALUE] [-r VALUE] [-k] [-h] [DIRECTORY]
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

### note:

make sure that your input directory consists *only* images.
dot-files, html, markdown and files w/o filetype extension are excluded: `.*`, `*.md`,`*.html` and `!*.*`
since Graphics Magick supports a wide array of image formats, there are no other exclusion of filetypes hardcoded.

## todo

- [ ] add support for multiple directories
- [ ] choose different background colors
- [ ] add easy html UI for previewing and generating the corresponding commandline
