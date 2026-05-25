# Camp Creek Lesson Plan Portal

This GitHub Pages project sends staff members to the correct SharePoint lesson plan folder.

## Files

- `index.html` - Page structure and JavaScript behavior.
- `style.css` - Camp Creek styling.
- `teachers.json` - School year, folder links, and teacher assignments.
- `Shield.png` / `Inverted-Shield.png` - Logo assets.

## Phase 2 Data Structure

The teacher list is now easier to maintain because folder links are stored once in the `folders` section, and each teacher is assigned to a `folderId`.

Example:

```json
{
  "folders": [
    {
      "id": "science",
      "label": "Science",
      "url": "https://sharepoint-folder-link"
    }
  ],
  "teachers": [
    {
      "name": "Teacher, Example",
      "email": "teachere@fultonschools.org",
      "folderId": "science"
    }
  ]
}
```

## Updating for a New School Year

1. Update `schoolYear`.
2. Review the `folders` section and replace SharePoint folder links if they change.
3. Add/remove teachers in the `teachers` section.
4. Make sure each teacher's `folderId` matches one of the IDs in the `folders` section.
5. Open the site with VS Code Live Server and test search, department filter, and folder redirects.
6. Commit and push changes in GitHub Desktop.

## Notes

- The page can still read the older Phase 1 array-style `teachers.json`, but the new object format is preferred.
- Use the `admin` section for admin-only/root lesson plan folder access.
- Teacher names are sorted automatically on the page.
