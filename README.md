# Embed Microsoft Teams chats in SharePoint pages

## Summary

This SPFx extension was built to embed Microsoft Teams chats within SharePoint pages to stramline collaboration and information access for users. This application customizer takes advantage of a Microsoft Teams integration made by Microsoft for Edge where links shared in chats open with the conversation context next to it in the browser. Using this solution you can bring the same feature to your SharePoint pages.

![Microsoft Teams chats in SharePoint](https://handsontek.net/images/GitHub/Microsoft%20Teams%20chat%20in%20SharePoint%20sites.gif)

## Used SharePoint Framework Version

![version](https://img.shields.io/badge/version-1.23.2-green.svg)

## Applies to

- [SharePoint Framework](https://aka.ms/spfx)

## Version history

| Version | Date             | Comments                                                                 |
| ------- | ---------------- | ------------------------------------------------------------------------ |
| 1.0     | November 19, 2023| Initial release                                                          |
| 1.1     | May 10, 2024     | Added support to render without granting Microsoft Graph permissions     |
| 2.0.    | August 25, 2026  | Architectural modernization: heft, spfx 1.23.2, node 24.19, npm v 12.0.2 |

## Disclaimer

**THIS CODE IS PROVIDED _AS IS_ WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**

---

## Minimal Path to Awesome

- Clone this repository
- Ensure that you are at the solution folder
- in the command-line run:
  - **npm install**
  - **heft run**

## Forking This Solution

If you're forking this repository for your own use, you **must** generate new GUIDs to avoid conflicts:

1. Run `npm install -g guid-typescript` (or use any GUID generator)
2. Generate 3 new GUIDs
3. Replace the GUIDs in these files:
   - **Solution ID**: `.yo-rc.json` (`libraryId`) and `config/package-solution.json` (`solution.id`)
   - **Extension ID**: `src/extensions/teamsChatEmbedded/TeamsChatEmbeddedApplicationCustomizer.manifest.json` (`id`), `config/serve.json` (`customActions` key), `sharepoint/assets/elements.xml` (`ClientSideComponentId`), `sharepoint/assets/ClientSideInstance.xml` (`ComponentId`)
   - **Feature ID**: `config/package-solution.json` (`features.id`)

Or run `guid` from Node:

```bash
node -e "console.log(require('crypto').randomUUID())"
```

## References

- [Building for Microsoft teams](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/build-for-teams-overview)
- [Use Microsoft Graph in your solution](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/web-parts/get-started/using-microsoft-graph-apis)
- [Publish SharePoint Framework applications to the Marketplace](https://docs.microsoft.com/en-us/sharepoint/dev/spfx/publish-to-marketplace-overview)
- [Microsoft 365 Patterns and Practices](https://aka.ms/m365pnp) - Guidance, tooling, samples and open-source controls for your Microsoft 365 development
