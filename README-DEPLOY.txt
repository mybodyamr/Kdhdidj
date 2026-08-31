Saudi Warehouse — Firebase sync v12

This version fixes the accidental saveState override that prevented Firestore writes.
It also persists warehouse task create/resolve/fail actions and bumps the PWA cache version.

Firebase projectId: saudi-warehouse
Firestore paths used:
- core/data
- reports/*
- leaves/*
- warehouseTasks/*
- shiftChanges/*

After deployment, hard-refresh/clear the old site cache once if the PWA keeps showing the old version.
