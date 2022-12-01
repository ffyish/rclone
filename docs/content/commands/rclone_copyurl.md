---
title: "rclone copyurl"
description: "Copy url content to dest."
slug: rclone_copyurl
url: /commands/rclone_copyurl/
# autogenerated - DO NOT EDIT, instead edit the source code in cmd/copyurl/ and as part of making a release run "make commanddocs"
---
# rclone copyurl

Copy url content to dest.

## Synopsis


Download a URL's content and copy it to the destination without saving
it in temporary storage.

Setting `--auto-filename` will attempt to automatically determine the filename from the URL
(after any redirections) and used in the destination path. 
With `--auto-filename-header` in 
addition, if a specific filename is set in HTTP headers, it will be used instead of the name from the URL.
With `--print-filename` in addition, the resulting file name will be printed.

Setting `--no-clobber` will prevent overwriting file on the 
destination if there is one with the same name.

Setting `--stdout` or making the output file name `-`
will cause the output to be written to standard output.


```
rclone copyurl https://example.com dest:path [flags]
```

## Options

```
  -a, --auto-filename     Get the file name from the URL and use it for destination file path
      --header-filename   Get the file name from the Content-Disposition header
  -h, --help              help for copyurl
      --no-clobber        Prevent overwriting file with same name
  -p, --print-filename    Print the resulting name from --auto-filename
      --stdout            Write the output to stdout rather than a file
```

See the [global flags page](/flags/) for global options not listed here.

## SEE ALSO

* [rclone](/commands/rclone/)	 - Show help for rclone commands, flags and backends.
