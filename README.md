<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />
<div align="center">

<h3 align="center">Dotfiles</h3>

  <p align="center">
    My dotfiles repo!
    <br />
    <br />
    <a href="https://github.com/inikolaou/.dotfiles/issues">Report Bug</a>
    ·
    <a href="https://github.com/inikolaou/.dotfiles/issues">Request Feature</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project
This is my dotfiles repository mainly based on https://github.com/josean-dev/dev-environment-files

<p align="right">(<a href="#readme-top">back to top</a>)</p>



### Built With

* [![Shell][Shell.com]][Shell-url]
* [![Lua][Lua.com]][Lua-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

To get started you need to have a pc with a unix operating system. Some tasks in the playbook are specific to the ubuntu distribution of linux. My dotfiles are about nvim, tmux, zsh and git. The .gitconfig file contains my personal details so if you decide to clone it you should replace my details with yours.

### Prerequisites
* First update and upgrade your package manager
  ```sh
  sudo apt update && sudo apt upgrade
  ```
* Make sure you have installed git
  ```sh
  sudo apt install git -y
  ```

### Installation
There are two ways to install the dotfiles
#### Direct install
All of the commands below were executed on ubuntu 22.04. Execute them based on your specific operating system and using your preferred package manager.

1. Clone the repo
   ```sh
   git clone https://github.com/inikolaou/.dotfiles.git ~/.dotfiles
   ```
2. Install zsh, neovim and tmux
   ```sh
   sudo apt install tmux zsh neovim -y
   ```
3. Install stow
   ```sh
   sudo apt install stow -y
   ```
4. Remove previously existing dotfiles
   ```sh
   rm ~/.gitconfig ~/.tmux.conf ~/.zshrc ~/.p10k.zsh
   ```
5. Remove nvim config folder
   ```sh
   rm -rf ~/.config/nvim
   ```
6. Stow dotfiles
   ```sh
   cd ~/.dotfiles && stow --restow */
   ```

#### Automatic install
If you don't want to manually type all these commands and also install some additional features you can check my other repository [pc-setup](https://github.com/inikolaou/pc-setup) and follow the instructions there.

### After Installation
Based on your terminal emulator you can choose a different color scheme file.

- Gnome Terminal
   ```sh
   dconf load /org/gnome/terminal/legacy/profiles:/ < ~/.dotfiles/gnome-terminal-profiles.dconf
   ```

- Windows Terminal
  Add to settings.json in schemes the json in `windows-terminal.colors`

- Iterm2
  Add the custom colorscheme `coolnight.itermcolors`

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTACT -->
## Contact

Project Link: [https://github.com/inikolaou/.dotfiles](https://github.com/inikolaou/.dotfiles)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* [Josean Martinez Dev Environment & Workflow](https://www.youtube.com/playlist?list=PLnu5gT9QrFg36OehOdECFvxFFeMHhb_07)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/inikolaou/.dotfiles.svg?style=for-the-badge
[contributors-url]: https://github.com/inikolaou/.dotfiles/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/inikolaou/.dotfiles.svg?style=for-the-badge
[forks-url]: https://github.com/inikolaou/.dotfiles/network/members
[stars-shield]: https://img.shields.io/github/stars/inikolaou/.dotfiles.svg?style=for-the-badge
[stars-url]: https://github.com/inikolaou/.dotfiles/stargazers
[issues-shield]: https://img.shields.io/github/issues/inikolaou/.dotfiles.svg?style=for-the-badge
[issues-url]: https://github.com/inikolaou/.dotfiles/issues
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/nikolaou-ioannis
[Shell.com]: https://img.shields.io/badge/Shell-black?style=for-the-badge&logo=gnubash&logoColor=white
[Shell-url]: https://www.gnu.org/software/bash/
[Lua.com]: https://img.shields.io/badge/Lua-darkblue?style=for-the-badge&logo=lua&logoColor=white
[Lua-url]: https://www.lua.org/