# Application Documentation (powered by DocFx)

## What is DocFX?

[DocFx](https://github.com/dotnet/docfx) is an open source project that helps buid documentation, with landing pages, [markdown](https://www.markdownguide.org/getting-started/), API reference docs for .NET, REST API and more.

## How to get started?

Click [here](https://dotnet.github.io/docfx/) to review DocFx Quick Start guide.

Click [here](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) to review markdown syntax.

## How was this sample doc site built?

1. Started with the default layout
2. Material-design classic template was added
3. Partial view was overwritten to add `Export to PDF` link

## How to run it?

1. Download `v2.62.1` from the [GitHub repo](https://github.com/dotnet/docfx/releases) for the target platform
2. Get latest from this repo
3. Make the needed/desired changes
4. Build and run it locally

## Steps to containerize doc site - Multi-stage builds

1. Get Microsoft .Net SDK base image
2. Download DocFX from GitHub repo
3. Unzip it
4. Clone doc site repo
5. Build docs
6. Get nginx base image
7. Copy built site to /usr/share/nginx/html
8. Map port 8080 to ngninx port 80
9. Connect to http://localhost:8080
