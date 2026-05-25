# Camp Creek Lesson Plan Portal

This GitHub Pages site redirects Camp Creek staff members to the correct lesson plan folder.

## Files

- `index.html` controls the page structure and redirect behavior.
- `style.css` controls the visual design.
- `teachers.json` stores the staff names, emails, and SharePoint folder links.
- `Shield.png` and `Inverted-Shield.png` are the logo assets.

## How to update the teacher list

1. Open `teachers.json`.
2. Add, remove, or edit teacher entries using this structure:

```json
{
  "name": "Last, First",
  "email": "username@fultonschools.org",
  "folder": "https://sharepoint-folder-link-here"
}
```

3. Confirm every entry has a `name` and `folder` value.
4. Save the file.
5. Commit and push the changes through GitHub Desktop.

## Notes

- The teacher list is sorted alphabetically on the page.
- Staff can search by name or email.
- The page now uses a confirmation button instead of redirecting immediately after selection.
- If the teacher list fails to load, staff are directed to email Mr. Gibson.
