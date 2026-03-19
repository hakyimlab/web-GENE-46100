# Git Commit Instructions

## Standard Commit with Co-Authors

```bash
git commit -m "$(cat <<'EOF'
<commit message here>

Co-Authored-By: Opencode
Co-Authored-By: Claude Code
EOF
)"
```

## Stage and Commit Specific Files

```bash
git add <file1> <file2>
git commit -m "$(cat <<'EOF'
<commit message here>

Co-Authored-By: Opencode
Co-Authored-By: Claude Code
EOF
)"
```

## Stage All Changes and Commit

```bash
git add -A
git commit -m "$(cat <<'EOF'
<commit message here>

Co-Authored-By: Opencode
Co-Authored-By: Claude Code
EOF
)"
```

## Notes

- Use heredoc (`<<'EOF'`) to preserve formatting and newlines in the commit message
- The blank line before `Co-Authored-By` is required for git to parse trailers correctly
- Check staged files before committing: `git status` and `git diff --staged`
