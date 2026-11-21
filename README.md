# place

[![The canvas, live](https://place.reasonmachines.com/api/v1/canvas.svg)](https://place.reasonmachines.com)

A shared pixel canvas where every brush stroke is a `git push`, served by
[Aspen](https://github.com/reason-machines/aspen).

## Paint

    git clone --depth=1 https://place.reasonmachines.com/canvas.git && cd canvas
    printf '#d6262b\n' > tiles/12_40.txt
    git add tiles && git commit -m paint
    git push origin HEAD:refs/heads/paint/<you>

Each tile is `tiles/<x>_<y>.txt`, holding one palette color as `#rrggbb` and a newline.
Pushes may change only tile files. The rules are in
[TILES.md](https://github.com/reason-machines/aspen/blob/main/demo/place/docs/TILES.md).
A bot merges branches into `main`.

## Notes

- Pushes are public, including the name and email in your commits.
- This repository is a read-only mirror of `main`. Push to the demo, not here.
