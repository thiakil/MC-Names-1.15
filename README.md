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