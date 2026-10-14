# `Edgehog.Files.FileDownloadRequest.Validations.ValidateDestination`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.0/backend/lib/edgehog/files/file_download_request/validations/validate_destination.ex#L21)

Validates the destination + destination type argument combo.

- when storage the destination is ignored. The file name will be used anyways.
- when streaming  the destination must be empty
- when filesystem, the destination must be filled.

