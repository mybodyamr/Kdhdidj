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
- pallets/*            (new: Pallet Management add-on)
- workerStatuses/*
- auditLog/*
- loadUnloadLog/*

Make sure Firestore Security Rules (firestore.rules) are deployed/published in
Firebase Console — this update adds rules for "pallets" plus three other
collections used by the app that had no rule before (workerStatuses, auditLog,
loadUnloadLog), which were silently failing to sync.

After deployment, hard-refresh/clear the old site cache once if the PWA keeps showing the old version.
