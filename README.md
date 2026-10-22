# Telegram Android Chat Folder Features

Four focused improvements for Telegram Android chat folders.

## Features

### Drag chats to folders

Select one or more chats and drag them directly to a folder tab. The interaction includes a compact drag preview, folder targeting, edge auto-scroll, drop feedback, and safe handling of pinned chats.

Patch:

```text
feature1/feature1_drag_to_folders.patch
```

### Quick New Folder

Adds a **New Folder** action to the main chats overflow menu and to the **All Chats** tab menu, opening Telegram's existing folder creation screen directly.

Patch:

```text
feature2/feature2_quick_new_folder.patch
```

### Add to folder with optional archiving

Patch:

```text
feature3/feature3_add_and_archive.patch
```

### Move and copy between folders

Patch:

```text
feature4/feature4_move_and_copy.patch
```

## Base version

The patches target Telegram Android 13.0.2 (7175), based on commit:

```text
f32ffeec763f0bdbf4bec25b52d654f77bff733d
```

Apply the patches from the Telegram Android repository root:

```bash
git apply /path/to/feature1_drag_to_folders.patch
git apply /path/to/feature2_quick_new_folder.patch
```

Features 1 and 2 are optional and remain independent. Feature 3 also applies directly to the base version. Apply Feature 4 **after Feature 3**: they share confirmed folder saving and Undo support.

For Features 3 and 4:

```bash
git apply --check /path/to/feature3_add_and_archive.patch
git apply /path/to/feature3_add_and_archive.patch
git apply --check /path/to/feature4_move_and_copy.patch
git apply /path/to/feature4_move_and_copy.patch
```

Existing account and server limits remain in effect. A manual folder cannot be left empty by Move; keep a chat in it or choose Copy. The existing Remove from folder action remains available under Telegram's original rules.

## License

Licensed under GPL-2.0, consistent with Telegram Android.

This is an independent contribution and is not an official Telegram product.
