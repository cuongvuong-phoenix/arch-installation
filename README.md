1. Install [**_EndeavourOS_**](https://endeavouros.com/):

- Before installing, download [`usr_pkglist.txt`](./usr_pkglist.txt) and place it in `~/home/liveuser` folder.
- While installing with **_Calamares_**, choose **_KDE_** as main desktop environment and remove some unnecessary packages:
  - `spectacle`
  - `elisa`
- After installing, do some extra works around [`usr_pkglist.txt`](./usr_pkglist.txt):
  - Configure packages that have comment attached with.
  - Install packages that are commented out.

3. Use [**_dotfiles_**](https://github.com/vuong-cuong-phoenix/dotfiles).
4. Configure **_KDE_**:

- Theme.
- **_Latte Dock_**:
  - Install required widgets:
    - [**_Event Calendar_**](https://store.kde.org/p/998901).
    - [**_Inline Battery_**](https://store.kde.org/p/1402942).
  - Apply layout by using [`bimbal.layout.latte`](./phoenix.layout.latte).
