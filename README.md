<div id="top"></div>

<!-- PROJECT SHIELDS -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links-->
<div align="center">

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

</div>

<!-- PROJECT HEADER -->
<div align="center">
  <h3 align="center">rewrk</h3>

  <p align="center">
    <i>Reworked wrk - Managed HTTP benchmarking tool</i>
    <br />
    <a href="https://github.com/proffapt/rewrk/issues">Request Feature | Report Bug</a>
  </p>
</div>


<!-- TABLE OF CONTENTS -->
<details>
<summary>Table of Contents</summary>

- [About The Project](#about-the-project)
  - [Supports](#supports)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
- [Contact](#contact)
- [Acknowledgements](#acknowledgments)
- [Additional documentation](#additional-documentation)

</details>


<!-- ABOUT THE PROJECT -->
## About The Project

Rewrk, a [wrk](https://github.com/wg/wrk) HTTP Benchmarking Wrapper Script, is designed to abstract the complexity of managing wrk processes. It provides functionality for both single benchmarking test and _sequential_ benchmarking as batch operations, provided via configuration file (.json), making load testing and benchmarking of HTTP servers straightforward.

<p align="right">(<a href="#top">back to top</a>)</p>

<div id="supports"></div>

### Supports:
1. OS(s)
    * `MacOS`[`BSD` based]
    * any `*nix`[`GNU+Linux` and `Unix`]

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- GETTING STARTED -->
## Getting Started

To set up a local instance of the application, follow the steps below.

### Prerequisites

The following dependencies are required to be installed for the project to function properly:
* `wrk`

  Follow the installation instructions for your platform for [wrk](https://github.com/wg/wrk).

* `jq`

  ```bash
  sudo apt install jq   # Ubuntu/Debian
  sudo yum install jq   # CentOS/Fedora
  brew install jq       # macOS (HomeBrew)
  ```

<p align="right">(<a href="#top">back to top</a>)</p>

### Installation

_Now that the environment has been set up and configured to properly compile and run the project, the next step is to install and configure the project locally on your system._
1. Clone the repository
   ```sh
   git clone https://github.com/proffapt/rewrk.git
   ```
2. Make the script executable
   ```sh
   cd ./rewrk
   chmod +x ./rewrk
   ```
3. Execute the script
   ```sh
   ./rewrk
   ```

<p align="right">(<a href="#top">back to top</a>)</p>


<!-- USAGE EXAMPLES -->
## Usage

```graphql
Usage: ./rewrk COMMAND [OPTIONS]

A wrapper script to manage wrk HTTP benchmarking tool

Commands:
  status                    Show the status of wrk process
  start ARGS                Start a single wrk instance with specified parameters
    Arguments:
      threads               Number of threads to use
      connections           Number of connections to keep open
      duration              Duration of the test (e.g., 30s, 1m, 1h)
      url                   Target URL
      [timeout]             Optional: Request timeout (default: 30s)

  stop                      Stop the running wrk process

  bstart ARGS               Start batch wrk processes using a configuration file
    Arguments:
      load_pattern_file     JSON file containing load patterns
      url                   Target URL
      [timeout]             Optional: Request timeout (default: 30s)

  bstop                     Stop all wrk processes in the batch

Example JSON load pattern file format:
{
  [
    {
      "threads": 1,
      "connections": 2,
      "duration": "1h"
    },
    {
      "threads": 1,
      "connections": 1,
      "duration": "1h"
    }
  ]
}

Examples:
  ./rewrk status
  ./rewrk start 1 2 10m http://example.com/load/1
  ./rewrk bstart load.example.json http://example.com/load/1
  ./rewrk stop
  ./rewrk bstop
```

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- CONTACT -->
## Contact

<p>
📫 Arpit Bhardwaj ( aka proffapt ) -
<a href="https://twitter.com/proffapt">
  <img align="center" alt="proffapt's Twitter " width="22px" src="https://raw.githubusercontent.com/edent/SuperTinyIcons/master/images/svg/twitter.svg" />
</a>
<a href="https://t.me/proffapt">
  <img align="center" alt="proffapt's Telegram" width="22px" src="https://raw.githubusercontent.com/edent/SuperTinyIcons/master/images/svg/telegram.svg" />
</a>
<a href="https://www.linkedin.com/in/proffapt/">
  <img align="center" alt="proffapt's LinkedIn" width="22px" src="https://raw.githubusercontent.com/edent/SuperTinyIcons/master/images/svg/linkedin.svg" />
</a>
<a href="mailto:proffapt@pm.me">
  <img align="center" alt="proffapt's mail" width="22px" src="https://raw.githubusercontent.com/edent/SuperTinyIcons/master/images/svg/mail.svg" />
</a>
<a href="https://cybernity.group">
  <img align="center" alt="proffapt's forum for cybernity" width="22px" src="https://cybernity.group/uploads/default/original/1X/a8338f86bbbedd39701c85d5f32cf3d817c04c27.png" />
</a>
</p>

<p align="right">(<a href="#top">back to top</a>)</p>


<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* [Choose an Open Source License](https://choosealicense.com)
* [Img Shields](https://shields.io)

<p align="right">(<a href="#top">back to top</a>)</p>

## Additional documentation

  - [Changelogs](/.github/CHANGELOG.md)
  - [License](/LICENSE)
  - [Security Policy](/.github/SECURITY.md)
  - [Code of Conduct](/.github/CODE_OF_CONDUCT.md)
  - [Contribution Guidelines](/.github/CONTRIBUTING.md)

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- MARKDOWN LINKS & IMAGES -->

[contributors-shield]: https://img.shields.io/github/contributors/proffapt/rewrk.svg?style=for-the-badge
[contributors-url]: https://github.com/proffapt/rewrk/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/proffapt/rewrk.svg?style=for-the-badge
[forks-url]: https://github.com/proffapt/rewrk/network/members
[stars-shield]: https://img.shields.io/github/stars/proffapt/rewrk.svg?style=for-the-badge
[stars-url]: https://github.com/proffapt/rewrk/stargazers
[issues-shield]: https://img.shields.io/github/issues/proffapt/rewrk.svg?style=for-the-badge
[issues-url]: https://github.com/proffapt/rewrk/issues
[license-shield]: https://img.shields.io/github/license/proffapt/rewrk.svg?style=for-the-badge
[license-url]: https://github.com/proffapt/rewrk/blob/master/LICENSE
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/proffapt
