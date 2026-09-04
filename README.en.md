# Codex Pets

[ภาษาไทย](README.md) | **English**

Custom animated pets for Codex, with character references, animation previews, and a workflow for creating new companions. The repository currently contains two pets.

This project keeps each pet's runtime files, character brief, reference images, and QA results together, making it easy to create and maintain pets in different styles within one repository.

## Pets

| Pet | Style | Format |
| --- | --- | --- |
| [Mira](pets/mira/README.md) | Anime elf with ash-blonde hair, black glasses, and a navy office uniform | v2 · 9 animations · 16 look directions |
| [Mori](pets/mori/README.md) | Humanoid 3D toy in olive techwear, cream sherpa fleece, and a black utility pouch | v2 · 9 animations · 16 look directions |

![Mira waving](pets/mira/qa/previews/waving.gif)
![Mori waving](pets/mori/qa/previews/waving.gif)

## Repository structure

```text
pets/
  <pet-id>/
    pet.json             # Codex pet metadata
    spritesheet.webp     # Final runtime atlas
    brief.json           # Character design and requirements
    README.md            # Usage and validation status
    qa/                  # Reports, contact sheets, and GIF previews
references/
  <pet-id>/              # Reference and approved concept images for each pet
docs/adding-a-pet.md      # Workflow for adding a new pet
templates/pet-brief.md    # Character brief template
```

Temporary generation files belong in `work/`, and packaged ZIP files belong in `dist/`. Both directories are excluded from Git.

## Use a pet

Choose a directory under `pets/`, place its `pet.json` and `spritesheet.webp` together in `~/.codex/pets/<pet-id>/`, then select the pet from Codex's pet controls when available.

Mira and Mori have passed atlas format validation and animation review. Selecting either pet in the Codex UI has not been tested. See the pages for [Mira](pets/mira/README.md) and [Mori](pets/mori/README.md) for details.

## Create another pet

Start with the [character brief template](templates/pet-brief.md), then follow the [guide to adding a pet](docs/adding-a-pet.md). Each pet has its own ID and directory, so multiple styles can be developed in the same repository.

Image creation uses the `hatch-pet` skill and the image generation tools available in Codex, installed separately from this repository. Finished pet files can be used without the image generation tools.

The linked pet documentation, workflow guide, and brief template are currently in Thai.
