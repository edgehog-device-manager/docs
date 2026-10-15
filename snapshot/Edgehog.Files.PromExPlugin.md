# `Edgehog.Files.PromExPlugin`
[🔗](https://github.com/edgehog-device-manager/edgehog/blob/v0.14.1/backend/lib/edgehog/files/prom_ex_plugin.ex#L21)

PromEx plugin for the Edgehog files feature.

Exposes the following metric groups:

- `:files_file_download_request_event_metrics` exposing the lifecycle of file download requests:
  - `edgehog_files_file_download_request_started_total`
  - `edgehog_files_file_download_request_completed_total` (labeled by `result`, `reason`)
  - `edgehog_files_file_download_request_duration_seconds` (labeled by `result`, `reason`)
  - `edgehog_files_file_download_request_retries`

- `:files_file_upload_request_event_metrics` exposing the lifecycle of file upload requests:
  - `edgehog_files_file_upload_request_started_total`
  - `edgehog_files_file_upload_request_completed_total` (labeled by `result`, `reason`)
  - `edgehog_files_file_upload_request_duration_seconds` (labeled by `result`, `reason`)
  - `edgehog_files_file_upload_request_retries`

