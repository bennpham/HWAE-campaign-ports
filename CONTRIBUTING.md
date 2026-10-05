# Contributing

Thanks for helping out! The converter gets campaigns most of the way to Anniversary Edition, but some things don't survive the trip: sprites can come out wrong, scripts can break, and levels can have missing or misplaced pieces. Fixes for any of that are welcome.

## What needs help

- **Art:** broken, missing, or misaligned sprites, tiles, doodads, and effects
- **Scripts and level logic:** triggers, doors, switches, and events that don't fire or don't behave like they did in the original
- **Gameplay:** enemies, items, or projectiles whose stats or behavior changed during conversion
- **Missing campaigns:** porting a campaign that isn't in the repo yet (see [Adding a new campaign](#adding-a-new-campaign))

If you're not sure whether something is a bug, open an issue that describes what you saw and, if you can, how it worked in the original game.

## Repo layout

```
original/<campaign>/    The original Hammerwatch files. Don't edit these.
converted/<campaign>/   The Anniversary Edition port. Make your fixes here.
```

`original/` is the reference copy. Keep it untouched so there's always something to compare against.

## Making a fix

1. Fork the repo and create a branch named after the campaign and the problem, e.g. `piratecove-fix-ship-sprites`.
2. Make your changes under `converted/<campaign>/`.
3. Test the campaign in Hammerwatch Anniversary Edition. Play through the part you changed, and make sure you didn't break anything around it.
4. Open a pull request that covers:
   - which campaign and which level(s) you changed
   - what was wrong and what you changed
   - screenshots for art fixes, ideally before and after

Keep each pull request to one campaign and one kind of fix. Small PRs are much easier to review.

## Is it a converter bug?

If the same problem shows up in several campaigns (for example, every campaign gets a certain sprite wrong), the real fix probably belongs in the converter:
[HammerwatchToAnniversaryCampaignConverter](https://github.com/bennpham/HammerwatchToAnniversaryCampaignConverter).

Report it there too, even if you also fix it by hand here. That way future conversions get it right automatically.

## Adding a new campaign

1. Find the original campaign on the Steam Workshop or, for older campaigns, on the [archived Hammerwatch forum](https://web.archive.org/web/20210116231406/http://hammerwatch.com/forum/index.php?board=2.0).
2. Put the unmodified files in `original/<campaign>/`.
3. Run the converter and put its output in `converted/<campaign>/`.
4. Commit the raw converter output first, then put any manual fixes in separate commits. That keeps it clear what the converter produced and what was fixed by hand.
5. In the PR description, include where you got the campaign from and who made it.

## Credit and permissions

These campaigns belong to their original authors. Don't strip author names or credits from campaign files. If you're the author of a campaign in this repo and want it changed or removed, open an issue.
