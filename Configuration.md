akashic-storage uses **typesafe config** for its configuration. You can change the backend, listening port etc by modifying `/opt/akashic-storage/etc/application.conf`.

The configuration would be something like this:

```
akashic.storage {
  backend {
    type = akashic.storage.backend.impl.Local
    mountpoint = /mnt/akashic-storage
  }

  # IP address or hostname to bind.
  ip = localhost

  # port to bind.
  port = 10946

  # akashic-storage uses Basic authentication scheme for the admin APIs.
  # Users need to add Authorization header to access admin APIs:
  # Authorization: Basic base64encode("admin:${admin-passwd}")
  admin-passwd = passwd
}
```