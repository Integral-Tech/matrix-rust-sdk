# Changelog

All notable changes to this project will be documented in this file.

## [0.8.0] - 2024-11-19

### Bug Fixes

- Disable `share_pos()` inside `RoomListService`.

- `UtdHookManager` no longer re-reports UTD events as late decryptions.
  ([#3480](https://github.com/matrix-org/matrix-rust-sdk/pull/3480))

- Messages that we were unable to decrypt no longer display a red padlock.
  ([#3956](https://github.com/matrix-org/matrix-rust-sdk/issues/3956))

- `UtdHookManager` no longer reports UTD events that were already reported in a
  previous session.
  ([#3519](https://github.com/matrix-org/matrix-rust-sdk/pull/3519))

### Features

- Add `m.room.join_rules` to the required state.

- `EncryptionSyncService` and `Notification` are using
  `Client::cross_process_store_locks_holder_name`.


### Refactor

- [**breaking**] `Timeline::edit` now takes a `RoomMessageEventContentWithoutRelation`.

- [**breaking**] `Timeline::send_attachment` now takes an `impl Into<PathBuf>`
  for the path of the file to send.

- [**breaking**] `Timeline::item_by_transaction_id` has been renamed to
  `Timeline::local_item_by_transaction_id` (always returns local echoes).


# 0.7.0

Initial release
