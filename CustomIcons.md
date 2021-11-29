# Making a Custom Icon Set
## File Stucture
- (MultiMC Directory)
  - iconthemes
      - custom
        - scalable
          - (Your Custom Icons)
        - index.theme
## Example Files/Image Names
### Images
Images should be in .svg (Scalable Vector Graphics) format.

        accounts.svg
        bug.svg
        cat.svg
        centralmods.svg
        checkupdate.svg
        copy.svg
        coremods.svg
        custom-commands.svg
        discord.svg
        externaltools.svg
        help.svg
        instance-settings.svg
        jarmods.svg
        java.svg
        language.svg
        launcher.svg
        loadermods.svg
        log.svg
        minecraft.svg
        new.svg
        news.svg
        notes.svg
        packages.svg
        patreon.svg
        proxy.svg
        quickmods.svg
        reddit-alien.svg
        refresh.svg
        resourcepacks.svg
        shaderpacks.svg
        screenshot-placeholder.svg
        screenshots.svg
        settings.svg
        star.svg
        status-bad.svg
        status-good.svg
        status-running.svg
        status-yellow.svg
        viewfolder.svg
        worlds.svg

### Example index.theme
    [Icon Theme]
    Name=(Theme Name)
    Comment=(Theme Comment)
    Inherits=multimc
    Directories=scalable

    [scalable]
    Size=48
    Type=Scalable
    MinSize=16
    MaxSize=256
