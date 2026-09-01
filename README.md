# Blender-GIT

This repository is configured for Blender projects:

- Primary `.blend` scene files are tracked with Git LFS because they are binary.
- `.blend` files are lockable, which helps avoid conflicting simultaneous edits.
- Blender's numbered backup files (for example `Scene.blend1`) stay local.

## One-time setup per collaborator

Install Git LFS, then enable it for your Git installation:

```powershell
git lfs install
```

## Typical workflow

Before editing a shared scene, lock it:

```powershell
git lfs lock MyScene.blend
```

Save in Blender, then commit and push as usual. When finished, unlock it:

```powershell
git lfs unlock MyScene.blend
```

For a new clone, retrieve the LFS files with:

```powershell
git lfs pull
```
