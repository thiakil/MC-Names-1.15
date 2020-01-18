Manual Mappings for Minecraft 1.15
===================================

In lieu of McpBotReborn not being updated to 1.15, and waiting on the new replacement (see Forge Discord), this repo serves as a manual point of collaboration between mod developers.

This repo contains additions to the 3 CSVs and a Gradle script to append those to the list from the McpBot 1.14.3 exports. Currently it can publish to your local maven, automation coming soon. 

These names will be offered to the McpBot replacement (meaning they may not accept them), so you must still follow any rules that would apply there.

- Do not submit any names you _know_ are "official" names; these will be rejected by the new service
    - Err on the side of not submitting a name if you know what the official name is
- Names should be verifiably based on the usage in code

## Names that exist in 1.14 but still unnamed
Please submit these via McpBot, the gradle task will pick them up.

## Quirks of this approach
- Param comments aren't automatically pulled across to the method's javadoc
    - This is something the bot normally pulls across
    - The `desc` field in params.csv is unused, serving only humans reading the file
- Name clashes will happen, please check your submissions via a forgegradle project before PRing (run a refresh twice so it does a recompile)

## Adding names
You may edit the files manually, but if you use IntelliJ IDEA, you are recommended to use [SRG Namer](https://github.com/thiakil/SrgNamer). Import the current CSV files and then start naming. Export to a clone of this repo, test, then make a PR!

## Using these names (manually)
1. Run the `publishToMavenLocal` task to publish to your local maven (usually `$HOME/.m2`)
2. Make sure you have `mavenLocal()` in your `repositories` block in `build.gradle`
3. Set your mappings version: `mappings channel: "snapshot", version: "<DATE>-github-1.15.1"`
4. Refresh project (twice to get sources attached)