# Notes for Claude on MCP GitHub Integration

## Current Issues (as of December 2024)

### File Operations
1. `create_or_update_file` function has persistent issues:
   - Error: "MCP error -32603: Invalid arguments: content.encoding: Required, content.content: Required"
   - Multiple attempts to fix content formatting and encoding haven't resolved the issue
   - This appears to be a limitation in the current MCP GitHub server implementation

### Working Solutions
1. Use `push_files` instead of `create_or_update_file`:
   ```javascript
   push_files({
     repo: "repo-name",
     files: [{path: "file/path", content: "content"}],
     owner: "owner-name",
     branch: "main",
     message: "commit message"
   })
   ```

### Configuration Notes
1. MCP server config should include:
   - Latest version of server-github package
   - Valid GitHub PAT with appropriate permissions
   - APPDATA environment variable
   - Debug flag for troubleshooting

### Best Practices
1. Always test basic read operations first (search_repositories, get_file_contents)
2. Use push_files for any write operations
3. Restart Claude Desktop app if changes are made to MCP configuration
4. Keep error messages for future reference and troubleshooting

### Future Improvements Needed
1. Proper support for content.encoding and content.content in create_or_update_file
2. Better error messaging for file operation failures
3. More detailed documentation on file operation requirements

### GitHub API Access
- Read operations work well (list repos, get contents)
- Write operations should use push_files
- Token permissions are critical - ensure full repo access

## Troubleshooting Steps
1. Verify GitHub token permissions
2. Check MCP server version
3. Restart Claude Desktop after config changes
4. Use DEBUG flag in config for more detailed error messages

Note: Keep this file updated as new issues or solutions are discovered.