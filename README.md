# 🔒 Google Apps Script: Make Google Docs Read-Only

This script uses **Google Apps Script** and the **Google Drive API** to make a Google Docs file read-only. It applies a `contentRestriction` on the file, preventing anyone (including editors) from editing the content, without changing their permissions.

---

## 🛠 What It Does

- Extracts the file ID from a shared Google Docs URL.
- Sends a `PATCH` request to the Drive API to apply a `readOnly` restriction.
- Locks the document against edits, even for editors and collaborators.
- Useful for freezing finalized documents or preventing accidental changes.

---

## ✅ Benefits Over Standard Viewer Access

> 💡 **How is this different from sharing the file as “Viewer”?**

| Feature                            | **Viewer Access**                                     | **Read-Only Restriction (via Script)**              |
|-----------------------------------|-------------------------------------------------------|-----------------------------------------------------|
| **Who can view**                  | Only users with the link or explicitly shared         | Same                                                |
| **Who can edit**                  | Only users with edit access                           | Same                                                |
| **Can editors still edit?**       | Yes, editors can still make changes                | No, even editors cannot edit unless restriction is removed |
| **Can be manually removed?**      | Yes, by changing access levels                     | Yes, but only manually or via script             |
| **Set manually in UI?**           | Yes                                               | No, must be done via API or script              |

This restriction allows you to **freeze a document** without changing roles or sharing settings.

---

