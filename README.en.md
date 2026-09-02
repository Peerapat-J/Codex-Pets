# Codex Pets

[ภาษาไทย](README.md) | **English**

Custom animated pets for Codex, with character references, animation previews, and a workflow for creating new companions.

This project keeps each pet's runtime files, character brief, reference images, and QA results together, making it easy to create and maintain pets in different styles within one repository.

## Pets

| Pet | Style | Format |
| --- | --- | --- |
| [Mira](pets/mira/README.md) | Anime elf with ash-blonde hair, black glasses, and a navy office uniform | v2 · 9 animations · 16 look directions |

![Mira waving](pets/mira/qa/previews/waving.gif)

## Repository structure

```text
pets/
  mira/
    pet.json             # Codex pet metadata
    spritesheet.webp     # Final runtime atlas
    brief.json           # Character design and requirements
    README.md            # Usage and validation status
    qa/                  # Reports, contact sheets, and GIF previews
references/
  mira/reference.png     # Original reference supplied by the user
docs/adding-a-pet.md      # Workflow for adding a new pet
templates/pet-brief.md    # Character brief template
```

Temporary generation files belong in `work/`, and packaged ZIP files belong in `dist/`. Both directories are excluded from Git.

## Use Mira

Place `pet.json` and `spritesheet.webp` from `pets/mira/` together in `~/.codex/pets/mira/`, then select Mira from Codex's pet controls when available.

Mira has passed atlas format validation and animation review. Selecting the pet in the Codex UI has not been tested. See [Mira's page](pets/mira/README.md) for details.

## Create another pet

Start with the [character brief template](templates/pet-brief.md), then follow the [guide to adding a pet](docs/adding-a-pet.md). Each pet has its own ID and directory, so multiple styles can be developed in the same repository.

Image creation uses the `hatch-pet` skill and the image generation tools available in Codex, installed separately from this repository. Finished pet files can be used without the image generation tools.

The linked pet documentation, workflow guide, and brief template are currently in Thai.
