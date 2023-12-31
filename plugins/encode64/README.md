# encode64

Alias plugin for encoding or decoding using `base64` command.

To use it, add `encode64` to the plugins array in your zshrc file:

```zsh
plugins=(... encode64)
```

## Functions and Aliases

| Function       | Alias  | Description                            |
| -------------- | ------ | -------------------------------------- |
| `encode64`     | `e64`  | Encodes given data to base64           |
| `encodefile64` | `ef64` | Encodes given file's content to base64 |
| `decode64`     | `d64`  | Decodes given data from base64         |

## Usage and examples

### Encoding

- From parameter

  ```console
  $ encode64 "coffeezhs"
  b2gtbXktenNo
  $ e64 "coffeezhs"
  b2gtbXktenNo
  ```

- From piping

  ```console
  $ echo "coffeezhs" | encode64
  b2gtbXktenNo==
  $ echo "coffeezhs" | e64
  b2gtbXktenNo==
  ```

### Encoding a file

Encode a file's contents to base64 and save output to text file.  
**NOTE:** Takes provided file and saves encoded content as new file with `.txt` extension

- From parameter

  ```console
  $ encodefile64 coffeezhs.icn
  coffeezhs.icn's content encoded in base64 and saved as coffeezhs.icn.txt
  $ ef64 "coffeezhs"
  coffeezhs.icn's content encoded in base64 and saved as coffeezhs.icn.txt
  ```

### Decoding

- From parameter

  ```console
  $ decode64 b2gtbXktenNo
  coffeezhs%
  $ d64 b2gtbXktenNo
  coffeezhs%
  ```

- From piping

  ```console
  $ echo "b2gtbXktenNoCg==" | decode64
  coffeezhs
  $ echo "b2gtbXktenNoCg==" | d64
  coffeezhs
  ```
