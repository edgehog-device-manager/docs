# `Edgehog.Files.Telemetry`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.0/backend/lib/edgehog/files/telemetry.ex#L21)

Edgehog file transfer telemetry.

Events can be emitted on the following topics:

- `[:edgehog, :files, :file_download_request, :start]` when a file download
  request provisioning starts. Metadata contains `transfer_type`, `destination_type`,
  `progress_tracked`, `needs_encoding`, `tenant_slug`, and optionally `request_id`, `device_id`,
  and `file_id`.
- `[:edgehog, :files, :file_download_request, :stop]` when a file download
  request terminates, either successfully or with a failure. Metadata contains
  the start metadata plus `result` (either `:ok` or `:error`), `reason` (either
  the provisioning outcome, e.g. `:ready` or `:already_ready`, or the failure reason),
  `duration` (native time), and `duration_unit` (`:native`). Measurements contain
  `count`, `duration` (native time), and `retries`.
- `[:edgehog, :files, :file_upload_request, :start]` when a file upload
  request starts. Metadata contains `transfer_type`, `source_type`,
  `progress_tracked`, `needs_encoding`, `tenant_slug`, and optionally `request_id` and `device_id`.
- `[:edgehog, :files, :file_upload_request, :stop]` when a file upload
  request terminates, either successfully or with a failure. Metadata contains
  the start metadata plus `result` (either `:ok` or `:error`), `reason`,
  `duration` (native time), and `duration_unit` (`:native`). Measurements contain
  `count`, `duration` (native time), and `retries`.

# `file_download_request_completed`

Emits a successful file download request stop event.

# `file_download_request_failed`

Emits a failed file download request stop event.

# `file_download_request_started`

Emits a file download request start event and returns the monotonic time the
download request started, to be used when emitting the corresponding stop event.

Returns the start time, computed with `System.monotonic_time/0`.

# `file_download_start_event`

# `file_download_stop_event`

# `file_upload_request_completed`

Emits a successful file upload request stop event.

# `file_upload_request_failed`

Emits a failed file upload request stop event.

# `file_upload_request_started`

Emits a file upload request start event and returns the monotonic time the
upload request started, to be used when emitting the corresponding stop event.

Returns the start time, computed with `System.monotonic_time/0`.

# `file_upload_start_event`

# `file_upload_stop_event`

# `include_identifiers?`

Returns true if telemetry identifiers should be included in event metadata.

