# fscrypt

This role can be used to setup encrypted filesystems on Linux with [fscrypt](https://github.com/google/fscrypt).

Since there is not Python library yet for using fscrypt, the role relies completely on the commandline utils.


## Example

```
  vars:
    fscrypt_encrypt_directories:
      - dir: "/mnt/crypt"
        user: secureuser
        password: "{{ secure_source }}"
    fscrypt_unlock_directories: "{{ fscrypt_encrypt_directories }}"

  roles:
    - fscrypt
```

See also [./defaults/main.yml](./defaults/main.yml) for more configurable variables.
