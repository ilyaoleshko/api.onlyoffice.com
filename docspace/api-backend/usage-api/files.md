# ONLYOFFICE DocSpace Files API

The browsable version of this reference, with a request builder and code samples, is published at
[https://api.onlyoffice.com/docspace/api-backend/usage-api/](https://api.onlyoffice.com/docspace/api-backend/usage-api/).

All URIs are relative to *https://yourportal.onlyoffice.com*, where the host is the address of your DocSpace instance.

## Files

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**addFileToRecent**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/add-file-to-recent.md) | **POST** /api/2.0/files/file/\{fileId\}/recent | Add a file to Recent |
| [**addTemplates**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/add-templates.md) | **POST** /api/2.0/files/templates | Add template files |
| [**changeVersionHistory**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/change-version-history.md) | **PUT** /api/2.0/files/file/\{fileId\}/history | Change version history |
| [**checkFillFormDraft**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/check-fill-form-draft.md) | **POST** /api/2.0/files/masterform/\{fileId\}/checkfillformdraft | Open a form draft for filling |
| [**copyFileAs**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/copy-file-as.md) | **POST** /api/2.0/files/file/\{fileId\}/copyas | Copy a file |
| [**createEditSession**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/create-edit-session.md) | **POST** /api/2.0/files/file/\{fileId\}/edit_session | Create the editing session |
| [**createFile**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/create-file.md) | **POST** /api/2.0/files/\{folderId\}/file | Create a file |
| [**createFileInMyDocuments**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/create-file-in-my-documents.md) | **POST** /api/2.0/files/@my/file | Create a file in My documents |
| [**createFilePrimaryExternalLink**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/create-file-primary-external-link.md) | **POST** /api/2.0/files/file/\{id\}/link | Create the file primary external link |
| [**createHtmlFile**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/create-html-file.md) | **POST** /api/2.0/files/\{folderId\}/html | Create an HTML file |
| [**createHtmlFileInMyDocuments**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/create-html-file-in-my-documents.md) | **POST** /api/2.0/files/@my/html | Create an HTML file in My documents |
| [**createTextFile**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/create-text-file.md) | **POST** /api/2.0/files/\{folderId\}/text | Create a text file |
| [**createTextFileInMyDocuments**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/create-text-file-in-my-documents.md) | **POST** /api/2.0/files/@my/text | Create a text file in My documents |
| [**createThumbnails**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/create-thumbnails.md) | **POST** /api/2.0/files/thumbnails | Queue file thumbnails |
| [**deleteFile**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/delete-file.md) | **DELETE** /api/2.0/files/file/\{fileId\} | Delete a file |
| [**deleteRecent**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/delete-recent.md) | **DELETE** /api/2.0/files/recent | Delete recent files |
| [**deleteTemplates**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/delete-templates.md) | **DELETE** /api/2.0/files/templates | Delete template files |
| [**generateXlsx**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/generate-xlsx.md) | **POST** /api/2.0/files/file/\{fileId\}/xlsx | Generate a form answers report |
| [**getAllFormRoles**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/get-all-form-roles.md) | **GET** /api/2.0/files/file/\{fileId\}/formroles | Get form roles |
| [**getEditDiffUrl**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/get-edit-diff-url.md) | **GET** /api/2.0/files/file/\{fileId\}/edit/diff | Get changes URL |
| [**getEditHistory**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/get-edit-history.md) | **GET** /api/2.0/files/file/\{fileId\}/edit/history | Get version history |
| [**getEncryptionInfo**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/get-encryption-info.md) | **GET** /api/2.0/files/\{fileId\}/access | Get file encryption information |
| [**getFileHistory**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/get-file-history.md) | **GET** /api/2.0/files/file/\{fileId\}/log | Get file history |
| [**getFileInfo**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/get-file-info.md) | **GET** /api/2.0/files/file/\{fileId\} | Get file information |
| [**getFileLinks**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/get-file-links.md) | **GET** /api/2.0/files/file/\{id\}/links | Get file external links |
| [**getFilePrimaryExternalLink**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/get-file-primary-external-link.md) | **GET** /api/2.0/files/file/\{id\}/link | Get the file primary external link |
| [**getFileVersionInfo**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/get-file-version-info.md) | **GET** /api/2.0/files/file/\{fileId\}/history | Get file versions |
| [**getFillResult**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/get-fill-result.md) | **GET** /api/2.0/files/file/fillresult | Get form-filling result |
| [**getFormSubmissions**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/get-form-submissions.md) | **GET** /api/2.0/files/file/\{fileId\}/submissions | Get form submission results |
| [**getPresignedFileUri**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/get-presigned-file-uri.md) | **GET** /api/2.0/files/file/\{fileId\}/presigned | Get a signed download address |
| [**getPresignedUri**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/get-presigned-uri.md) | **GET** /api/2.0/files/file/\{fileId\}/presigneduri | Get file download link |
| [**getProtectedFileUsers**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/get-protected-file-users.md) | **GET** /api/2.0/files/file/\{fileId\}/protectusers | Get users for document protection |
| [**getReferenceData**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/get-reference-data.md) | **POST** /api/2.0/files/file/referencedata | Resolve a spreadsheet reference |
| [**getXlsx**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/get-xlsx.md) | **GET** /api/2.0/files/file/\{fileId\}/xlsx | Get form report generation status |
| [**isFormPDF**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/is-form-pdf.md) | **GET** /api/2.0/files/file/\{fileId\}/isformpdf | Check the PDF file |
| [**lockFile**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/lock-file.md) | **PUT** /api/2.0/files/file/\{fileId\}/lock | Lock a file |
| [**manageFormFilling**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/manage-form-filling.md) | **PUT** /api/2.0/files/file/\{fileId\}/manageformfilling | Perform form filling action |
| [**openEditFile**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/open-edit-file.md) | **GET** /api/2.0/files/file/\{fileId\}/openedit | Get the editor configuration |
| [**restoreFileVersion**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/restore-file-version.md) | **POST** /api/2.0/files/file/\{fileId\}/restoreversion | Restore a file version |
| [**saveEditingFileFromForm**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/save-editing-file-from-form.md) | **PUT** /api/2.0/files/file/\{fileId\}/saveediting | Save edited file content |
| [**saveFileAsPdf**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/save-file-as-pdf.md) | **POST** /api/2.0/files/file/\{id\}/saveaspdf | Save a file as PDF |
| [**saveFormRoleMapping**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/save-form-role-mapping.md) | **POST** /api/2.0/files/file/\{fileId\}/formrolemapping | Save form role mapping |
| [**setCustomFilterTag**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/set-custom-filter-tag.md) | **PUT** /api/2.0/files/file/\{fileId\}/customfilter | Set the Custom Filter editing mode |
| [**setEncryptionInfo**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/set-encryption-info.md) | **PUT** /api/2.0/files/\{fileId\}/access | Set file encryption information |
| [**setFileExternalLink**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/set-file-external-link.md) | **PUT** /api/2.0/files/file/\{id\}/links | Set a file external link |
| [**setFileOrder**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/set-file-order.md) | **PUT** /api/2.0/files/\{fileId\}/order | Set file order |
| [**setFilesOrder**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/set-files-order.md) | **PUT** /api/2.0/files/order | Set order of files |
| [**startEditFile**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/start-edit-file.md) | **POST** /api/2.0/files/file/\{fileId\}/startedit | Open an editing session |
| [**startFillingFile**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/start-filling-file.md) | **PUT** /api/2.0/files/file/\{fileId\}/startfilling | Start filling a form |
| [**toggleFileFavorite**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/toggle-file-favorite.md) | **GET** /api/2.0/files/favorites/\{fileId\} | Set the file favorite status |
| [**trackEditFile**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/track-edit-file.md) | **GET** /api/2.0/files/file/\{fileId\}/trackeditfile | Track an editing session |
| [**updateFile**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/files/update-file.md) | **PUT** /api/2.0/files/file/\{fileId\} | Update a file |

## Folders

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**checkUpload**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/check-upload.md) | **POST** /api/2.0/files/\{folderId\}/upload/check | Check for upload conflicts |
| [**createFolder**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/create-folder.md) | **POST** /api/2.0/files/folder/\{folderId\} | Create a folder |
| [**createFolderPrimaryExternalLink**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/create-folder-primary-external-link.md) | **POST** /api/2.0/files/folder/\{id\}/link | Create the folder primary external link |
| [**createReportFolderHistory**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/create-report-folder-history.md) | **POST** /api/2.0/files/folder/\{folderId\}/log/report | Start the folder history report generation |
| [**deleteFolder**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/delete-folder.md) | **DELETE** /api/2.0/files/folder/\{folderId\} | Delete a folder |
| [**generateXlsxByFolder**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/generate-xlsx-by-folder.md) | **POST** /api/2.0/files/folder/\{folderId\}/xlsx | Generate XLSX report by folder |
| [**getFavoritesFolder**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/get-favorites-folder.md) | **GET** /api/2.0/files/@favorites | Get the Favorites section |
| [**getFilesUsedSpace**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/get-files-used-space.md) | **GET** /api/2.0/files/filesusedspace | Get used space of files |
| [**getFolder**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/get-folder.md) | **GET** /api/2.0/files/\{folderId\}/formfilter | Get folder form filter |
| [**getFolderByFolderId**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/get-folder-by-folder-id.md) | **GET** /api/2.0/files/\{folderId\} | Get a folder by ID |
| [**getFolderHistory**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/get-folder-history.md) | **GET** /api/2.0/files/folder/\{folderId\}/log | Get folder history |
| [**getFolderInfo**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/get-folder-info.md) | **GET** /api/2.0/files/folder/\{folderId\} | Get folder information |
| [**getFolderLinks**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/get-folder-links.md) | **GET** /api/2.0/files/folder/\{id\}/links | Get folder external links |
| [**getFolderPath**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/get-folder-path.md) | **GET** /api/2.0/files/folder/\{folderId\}/path | Get the folder path |
| [**getFolderPrimaryExternalLink**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/get-folder-primary-external-link.md) | **GET** /api/2.0/files/folder/\{id\}/link | Get the folder primary external link |
| [**getFolders**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/get-folders.md) | **GET** /api/2.0/files/\{folderId\}/subfolders | Get subfolders |
| [**getFormsFolder**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/get-forms-folder.md) | **GET** /api/2.0/files/@forms | Get the Forms section |
| [**getMyFolder**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/get-my-folder.md) | **GET** /api/2.0/files/@my | Get the My documents section |
| [**getNewFolderItems**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/get-new-folder-items.md) | **GET** /api/2.0/files/\{folderId\}/news | Get new folder items |
| [**getRecentFolder**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/get-recent-folder.md) | **GET** /api/2.0/files/recent | Get the Recent section |
| [**getReportFolderHistory**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/get-report-folder-history.md) | **GET** /api/2.0/files/folder/\{folderId\}/log/report | Get the folder history report generation status |
| [**getRootFolders**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/get-root-folders.md) | **GET** /api/2.0/files/@root | Get filtered sections |
| [**getTrashFolder**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/get-trash-folder.md) | **GET** /api/2.0/files/@trash | Get the Trash section |
| [**insertFile**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/insert-file.md) | **POST** /api/2.0/files/\{folderId\}/insert | Insert a file |
| [**insertFileToMyFromBody**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/insert-file-to-my-from-body.md) | **POST** /api/2.0/files/@my/insert | Insert a file into My documents |
| [**renameFolder**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/rename-folder.md) | **PUT** /api/2.0/files/folder/\{folderId\} | Rename a folder |
| [**setFolderOrder**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/set-folder-order.md) | **PUT** /api/2.0/files/folder/\{folderId\}/order | Set folder order |
| [**setFolderPrimaryExternalLink**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/set-folder-primary-external-link.md) | **PUT** /api/2.0/files/folder/\{id\}/links | Set the folder external link |
| [**terminateReportFolderHistory**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/terminate-report-folder-history.md) | **DELETE** /api/2.0/files/folder/\{folderId\}/log/report | Terminate the folder history report generation |
| [**uploadFile**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/upload-file.md) | **POST** /api/2.0/files/\{folderId\}/upload | Upload a file |
| [**uploadFileToMy**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/folders/upload-file-to-my.md) | **POST** /api/2.0/files/@my/upload | Upload a file to My documents |

## Operations

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**abortUploadSession**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/operations/abort-upload-session.md) | **DELETE** /api/2.0/files/\{folderId\}/session/\{sessionId\} | Abort an upload session |
| [**addFavorites**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/operations/add-favorites.md) | **POST** /api/2.0/files/favorites | Add favorite files and folders |
| [**bulkDownload**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/operations/bulk-download.md) | **PUT** /api/2.0/files/fileops/bulkdownload | Bulk download |
| [**checkConversionStatus**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/operations/check-conversion-status.md) | **GET** /api/2.0/files/file/\{fileId\}/checkconversion | Get conversion status |
| [**checkMoveOrCopyBatchItems**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/operations/check-move-or-copy-batch-items.md) | **GET** /api/2.0/files/fileops/move | Check move or copy conflicts |
| [**checkMoveOrCopyDestFolder**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/operations/check-move-or-copy-dest-folder.md) | **GET** /api/2.0/files/fileops/checkdestfolder | Check the destination folder |
| [**copyBatchItems**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/operations/copy-batch-items.md) | **PUT** /api/2.0/files/fileops/copy | Copy files and folders |
| [**createUploadSession**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/operations/create-upload-session.md) | **POST** /api/2.0/files/\{folderId\}/upload/create_session | Chunked upload |
| [**createUploadSessionInFolder**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/operations/create-upload-session-in-folder.md) | **POST** /api/2.0/files/\{folderId\}/session | Create an upload session |
| [**deleteBatchItems**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/operations/delete-batch-items.md) | **PUT** /api/2.0/files/fileops/delete | Delete files and folders |
| [**deleteFavoritesFromBody**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/operations/delete-favorites-from-body.md) | **DELETE** /api/2.0/files/favorites | Delete favorite files and folders |
| [**deleteFileVersions**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/operations/delete-file-versions.md) | **PUT** /api/2.0/files/fileops/deleteversion | Delete file versions |
| [**duplicateBatchItems**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/operations/duplicate-batch-items.md) | **PUT** /api/2.0/files/fileops/duplicate | Duplicate files and folders |
| [**emptyTrash**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/operations/empty-trash.md) | **PUT** /api/2.0/files/fileops/emptytrash | Empty the Trash folder |
| [**finalizeSession**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/operations/finalize-session.md) | **PUT** /api/2.0/files/\{folderId\}/session/\{sessionId\}/finalize | Finalize an upload session |
| [**getOperationStatuses**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/operations/get-operation-statuses.md) | **GET** /api/2.0/files/fileops | Get active file operations |
| [**getOperationStatusesByType**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/operations/get-operation-statuses-by-type.md) | **GET** /api/2.0/files/fileops/\{operationType\} | Get file operations by type |
| [**markAsRead**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/operations/mark-as-read.md) | **PUT** /api/2.0/files/fileops/markasread | Mark files and folders as read |
| [**moveBatchItems**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/operations/move-batch-items.md) | **PUT** /api/2.0/files/fileops/move | Move files and folders |
| [**startFileConversion**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/operations/start-file-conversion.md) | **PUT** /api/2.0/files/file/\{fileId\}/checkconversion | Start file conversion |
| [**terminateTasks**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/operations/terminate-tasks.md) | **PUT** /api/2.0/files/fileops/terminate/\{id\} | Cancel file operations |
| [**updateFileComment**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/operations/update-file-comment.md) | **PUT** /api/2.0/files/file/\{fileId\}/comment | Update a comment |
| [**uploadAsyncSession**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/operations/upload-async-session.md) | **POST** /api/2.0/files/\{folderId\}/session/\{sessionId\}/upload | Upload a numbered chunk |
| [**uploadSession**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/operations/upload-session.md) | **POST** /api/2.0/files/\{folderId\}/session/\{sessionId\} | Upload the next chunk |

## Quota

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**resetRoomQuota**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/quota/reset-room-quota.md) | **PUT** /api/2.0/files/rooms/resetquota | Reset the room quota limit |
| [**updateRoomsQuota**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/quota/update-rooms-quota.md) | **PUT** /api/2.0/files/rooms/roomquota | Change the room quota limit |

## Settings

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**changeAccessToThirdparty**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/change-access-to-thirdparty.md) | **PUT** /api/2.0/files/thirdparty | Change the third-party settings access |
| [**changeAutomaticallyCleanUp**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/change-automatically-clean-up.md) | **PUT** /api/2.0/files/settings/autocleanup | Update the trash bin auto-clearing setting |
| [**changeDefaultAccessRights**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/change-default-access-rights.md) | **PUT** /api/2.0/files/settings/dafaultaccessrights | Change the default access rights |
| [**changeDeleteConfirm**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/change-delete-confirm.md) | **PUT** /api/2.0/files/changedeleteconfrim | Ask for delete confirmation |
| [**changeDownloadZip**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/change-download-zip.md) | **PUT** /api/2.0/files/settings/downloadtargz | Change the download archive format |
| [**changeExternalSharingSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/change-external-sharing-settings.md) | **PUT** /api/2.0/files/settings/externalsharingsettings | Configure external sharing |
| [**checkDocServiceUrl**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/check-doc-service-url.md) | **PUT** /api/2.0/files/docservice | Set the document service address |
| [**displayFileExtension**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/display-file-extension.md) | **PUT** /api/2.0/files/displayfileextension | Display a file extension |
| [**displayRecent**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/display-recent.md) | **PUT** /api/2.0/files/displayrecent | Show the Recent section |
| [**externalShare**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/external-share.md) | **PUT** /api/2.0/files/settings/external | Change the external sharing ability |
| [**externalShareSocialMedia**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/external-share-social-media.md) | **PUT** /api/2.0/files/settings/externalsocialmedia | Change the external sharing ability on social networks |
| [**forcesave**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/forcesave.md) | **PUT** /api/2.0/files/forcesave | Change the forcesaving ability |
| [**getAutomaticallyCleanUp**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/get-automatically-clean-up.md) | **GET** /api/2.0/files/settings/autocleanup | Get the trash bin auto-clearing setting |
| [**getDefaultTemplates**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/get-default-templates.md) | **GET** /api/2.0/files/settings/defaulttemplate | Get the default template setting |
| [**getDocServiceUrl**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/get-doc-service-url.md) | **GET** /api/2.0/files/docservice | Get the document service address |
| [**getFilesModule**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/get-files-module.md) | **GET** /api/2.0/files/info | Get the Documents module information |
| [**getFilesSettings**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/get-files-settings.md) | **GET** /api/2.0/files/settings | Get file settings |
| [**hideConfirmCancelOperation**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/hide-confirm-cancel-operation.md) | **PUT** /api/2.0/files/hideconfirmcanceloperation | Hide confirmation dialog when canceling operations |
| [**hideConfirmConvert**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/hide-confirm-convert.md) | **PUT** /api/2.0/files/hideconfirmconvert | Hide the confirmation dialog when converting |
| [**hideConfirmRoomLifetime**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/hide-confirm-room-lifetime.md) | **PUT** /api/2.0/files/hideconfirmroomlifetime | Hide confirmation dialog when changing room lifetime settings |
| [**keepNewFileName**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/keep-new-file-name.md) | **PUT** /api/2.0/files/keepnewfilename | Keep the default file name |
| [**resetDefaultTemplate**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/reset-default-template.md) | **DELETE** /api/2.0/files/settings/defaulttemplate | Reset the default template setting |
| [**setDefaultTemplate**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/set-default-template.md) | **PUT** /api/2.0/files/settings/defaulttemplate | Change the default template setting |
| [**setOpenEditorInSameTab**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/set-open-editor-in-same-tab.md) | **PUT** /api/2.0/files/settings/openeditorinsametab | Open document in the same browser tab |
| [**setOrganizeRoomsGrouping**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/set-organize-rooms-grouping.md) | **PUT** /api/2.0/files/settings/organizegrouping | Organize rooms grouping |
| [**showQuickActions**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/show-quick-actions.md) | **PUT** /api/2.0/files/showquickactions | Display quick actions |
| [**storeForcesave**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/store-forcesave.md) | **PUT** /api/2.0/files/storeforcesave | Change the ability to store the forcesaved files |
| [**storeOriginal**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/store-original.md) | **PUT** /api/2.0/files/storeoriginal | Change the ability to upload original formats |
| [**updateFileIfExist**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/update-file-if-exist.md) | **PUT** /api/2.0/files/updateifexist | Update a file version if it exists |
| [**uploadDefaultTemplate**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/settings/upload-default-template.md) | **POST** /api/2.0/files/settings/defaulttemplate | Upload a file as the default template setting |

## Sharing

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**applyExternalSharePassword**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/sharing/apply-external-share-password.md) | **POST** /api/2.0/files/share/\{key\}/password | Unlock a password-protected link |
| [**changeFileOwner**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/sharing/change-file-owner.md) | **POST** /api/2.0/files/owner | Change the room or file owner |
| [**getEncryptionAccess**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/sharing/get-encryption-access.md) | **GET** /api/2.0/files/file/\{fileId\}/publickeys | Get file encryption keys |
| [**getExternalShareData**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/sharing/get-external-share-data.md) | **GET** /api/2.0/files/share/\{key\} | Resolve an external share link |
| [**getFileSecurityInfo**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/sharing/get-file-security-info.md) | **GET** /api/2.0/files/file/\{id\}/share | Get file sharing rights |
| [**getFolderSecurityInfo**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/sharing/get-folder-security-info.md) | **GET** /api/2.0/files/folder/\{id\}/share | Get folder sharing rights |
| [**getGroupsMembersWithFileSecurity**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/sharing/get-groups-members-with-file-security.md) | **GET** /api/2.0/files/file/\{fileId\}/group/\{groupId\}/share | Get file access of group members |
| [**getGroupsMembersWithFolderSecurity**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/sharing/get-groups-members-with-folder-security.md) | **GET** /api/2.0/files/folder/\{folderId\}/group/\{groupId\}/share | Get folder access of group members |
| [**getSecurityInfo**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/sharing/get-security-info.md) | **POST** /api/2.0/files/share | Get sharing rights in batch |
| [**getSharedUsers**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/sharing/get-shared-users.md) | **GET** /api/2.0/files/file/\{fileId\}/sharedusers | Get users to mention in a file |
| [**removeSecurityInfo**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/sharing/remove-security-info.md) | **DELETE** /api/2.0/files/share | Remove sharing rights in batch |
| [**sendEditorNotify**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/sharing/send-editor-notify.md) | **POST** /api/2.0/files/file/\{fileId\}/sendeditornotify | Notify mentioned users |
| [**setFileSecurityInfo**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/sharing/set-file-security-info.md) | **PUT** /api/2.0/files/file/\{id\}/share | Share a file |
| [**setFolderSecurityInfo**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/sharing/set-folder-security-info.md) | **PUT** /api/2.0/files/folder/\{id\}/share | Share a folder |
| [**setSecurityInfo**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/sharing/set-security-info.md) | **PUT** /api/2.0/files/share | Set sharing rights in batch |

## Third-party integration

| Method | HTTP request | Description |
|------------ | ------------- | -------------|
| [**deleteThirdParty**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/third-party-integration/delete-third-party.md) | **DELETE** /api/2.0/files/thirdparty/\{providerId\} | Remove a third-party account |
| [**getAllProviders**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/third-party-integration/get-all-providers.md) | **GET** /api/2.0/files/thirdparty/providers | Get all third-party providers |
| [**getBackupThirdPartyAccount**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/third-party-integration/get-backup-third-party-account.md) | **GET** /api/2.0/files/thirdparty/backup | Get the third-party backup folder |
| [**getCapabilities**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/third-party-integration/get-capabilities.md) | **GET** /api/2.0/files/thirdparty/capabilities | Get third-party provider capabilities |
| [**getCommonThirdPartyFolders**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/third-party-integration/get-common-third-party-folders.md) | **GET** /api/2.0/files/thirdparty/common | Get common third-party folders |
| [**getThirdPartyAccounts**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/third-party-integration/get-third-party-accounts.md) | **GET** /api/2.0/files/thirdparty | Get the third-party accounts |
| [**saveThirdParty**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/third-party-integration/save-third-party.md) | **POST** /api/2.0/files/thirdparty | Connect a third-party account |
| [**saveThirdPartyBackup**](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/api-backend/usage-api/files/third-party-integration/save-third-party-backup.md) | **POST** /api/2.0/files/thirdparty/backup | Connect the third-party backup storage |

## Authorization

### cookieAuth
- **Type**: API key
- **API key parameter name**: asc_auth_key
- **Location**: 

### bearerAuth

- **Type**: HTTP Bearer Token authentication

### asc_auth_key
- **Type**: API key
- **API key parameter name**: asc_auth_key
- **Location**: 

### Basic

- **Type**: HTTP basic authentication

### Bearer

- **Type**: HTTP Bearer Token authentication (JWT)

### ApiKeyBearer
- **Type**: API key
- **API key parameter name**: ApiKeyBearer
- **Location**: HTTP header

### OAuth2

- **Type**: OAuth
- **Flow**: accessCode
- **Authorization URL**: 
- **Scopes**: 
  - read: Read access to protected resources
  - write: Write access to protected resources

### OpenId

### x-signature
- **Type**: API key
- **API key parameter name**: x-signature
- **Location**: 

