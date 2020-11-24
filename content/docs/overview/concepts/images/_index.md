---
title: "Analyzing Images"
linkTitle: "Images"
weight: 1
---

Once an image is submitted to Anchore Enterprise for analysis, Anchore Enterprise will attempt to retrieve metadata about the image from the Docker registry and if successful will download the image and queue the image for analysis.

Anchore Enterprise can run one or more analyzer services to scale out processing of images. The next available analyzer worker will process the image.

![alt text](AnalyzingImages.png)

During analysis every package, software library and file are inspected and this data is stored in the Anchore Database.

Anchore Enterprise includes a number of analyzer modules that extract data from the image including:

- Image metadata
- Image layers
- Operating System Package Data (RPM, DEB, APKG)
- File Data
- Ruby Gems
- Node.JS NPMs
- Java Archives
- Python Packages
- .NET NuGet Packages
- File content

Once a tag has been added to Anchore Enterprise the repository will be monitored for updates to that tag.

Any updated images will be downloaded and analyzed.

### Next Steps

Now let's get familiar with the [Image Analysis Process]({{< ref "/docs/overview/concepts/images/analysis" >}}).
