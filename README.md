# nbr.keymap

A scope-based keymap system for modal editors that organizes mappings based on their contextual scope rather than by tool or function.

## Philosophy

Traditional modal editor keymaps typically organize bindings by tool (git, LSP, etc.) or function. This system takes a different approach by organizing mappings based on their scope of operation:

- **Workspace** (`<leader>w`) - Operations affecting the entire workspace
- **Document** (`<leader>d`) - Operations on the current document
- **Symbol** (`<leader>s`) - Operations on code symbols
- **Hunks** (`<leader>h`) - Operations on code chunks/hunks
- **App** (`<leader>a`) - Application-level operations

## Design Principles

1. **Scope First**:

- Every operation must clearly belong to a specific scope (workspace, document, symbol)
- The scope should be immediately obvious from the operation's nature
- Operations affecting multiple scopes should be carefully considered

2. **Semantic Operations**:

- Mappings should represent clear, meaningful operations
- Focus on frequently used operations that benefit from quick access
- Operations should be distinct from basic editor commands
- Focus on what the operation means, not how it's implemented

3. **Tool & Editor Agnostic**:

- Mappings should be independent of specific tools or editors
- Use semantic terms (e.g., 'version' instead of 'git')
- Implementation details are left to the user's configuration

4. **Preserve Editor Defaults**:

- Don't replace basic editor operations with custom mappings
- Focus on operations that enhance rather than replace core functionality
- Leave common editor commands in their traditional form

5. **Consistent Patterns**:

- Second key should relate to the action within the scope
- Related operations should share the same scope
- Maintain predictable patterns across all mappings

6. **Single Source**:

- Each operation should have exactly one mapping
- Avoid duplicate mappings across different key combinations
- Choose the most appropriate and efficient mapping location

## Keymap Documentation

[See the complete keymap documentation here.](KEYMAP.md)

## Contributing

Feel free to:

- Suggest improvements to the scope organization
- Propose new scopes for uncovered contexts
- Share your adaptations for different editors

## License

MIT License - Feel free to adapt and use in your own configurations.
