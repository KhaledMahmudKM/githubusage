# Undoing Changes and Recovery

## Discard Local Changes

```bash
git restore file.txt
```

## Reset Commits

```bash
git reset --soft HEAD~1
git reset --hard HEAD~1
```

## Reverting a Commit

```bash
git revert <commit-hash>
```

## Using reflog

```bash
git reflog
```

---