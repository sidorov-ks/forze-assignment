# `bayan`

A command-line utility for search duplicate files. Command-line arguments:

- `--scan-dir <dir>`: `bayan` will search through files in directory `<dir>`. May be used multiple times to specify different directories for the search. Defaults to the launch path.
- `--depth <d>`: sets the search depth. For example, `--depth 0` search over files within `--scan-dir`, `--depth 1` will also consider files in subdirectories of `--scan-dir` and so on.
- `--exclude-dir <dir>`: `bayan` will not consider the directory `<dir>` and its contents.
- `--min-bytes <s>`: minimum file size in bytes.
- `--filename-masks <mask1> <mask2> ...`: if set will scan only through files with filenames satisfying one of the mask `<mask1>`, `<mask2>`, ...
- `--block-size <block>`: file contents are read by blocks of `<block>` bytes.
- `--hash {md5, sha256}`: specifies the hashing algorithm for the block. Block hash is used to check whether the files have the same content.