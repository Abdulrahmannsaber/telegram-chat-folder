# Telegram Android Chat Folder Features

Two focused improvements for Telegram Android chat folders.

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

## License

Licensed under GPL-2.0, consistent with Telegram Android.

This is an independent contribution and is not an official Telegram product.
