### Recap:

- To open and use your encrypted container:
  ```bash
  sudo cryptsetup open ~/encrypted_container.img encrypted_misc
  ```
- Once opened, you can mount it, use the files, and then unmount and close it when you're done to keep it secure:
  ```bash
  sudo mount /dev/mapper/encrypted_misc ~/encrypted_misc
  # Work with your files...
  sudo umount ~/encrypted_misc
  sudo cryptsetup close encrypted_misc
  ```
