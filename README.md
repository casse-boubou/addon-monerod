# Home Assistant Add-on: Monerod

[![GitHub Release][releases-shield]][releases]
[![License][license-shield]](LICENSE)

![Supports aarch64 Architecture][aarch64-shield]

[Monerod][getmonero] executera un noeud monero sur votre instance créant ainsi
une copie complète de la blockchain Monero et participant activement à la
sécuritée du réseau.

[![Open your Home Assistant instance and show the add add-on repository dialog
with a specific repository URL pre-filled.][add-repo-shield]][add-repo]
[![Open your Home Assistant instance and show the dashboard of a Supervisor add-on.][add-addon-shield]][add-addon]

## About

- Vérifiez que le port 18080 (Monero p2p port) soit ouvert dans votre pare-feu pour
  assurer une meilleure connectivité. Si vous exploitez une machine derrière NAT
  (comme un routeur), vous pouvez envisager de transférer les ports vers votre
  machine local.
- L'execution de monerod copiera l'integralitée de la blockchain Monero sur le disque
  de votre machine. Assurez-vous d'avoir la place necessaire disponible sur votre
  disque. Vous pouvez économiser 2/3 de la place necessaire à la blockchain en
  utilisant l'option `sync_pruned_blocks` qui telechargera alors une version
  [Pruned][pruning] de la blockchain.
- Cet addon est essentielement develloper pour être utiliser avec [P2pool][p2pool].
  Vous pouvez utiliser mon autre [addon P2pool][addon_p2pool] pour HomeAssistant.
  Ou télécharger les fichiers binaires officiels de [P2pool][p2pool], executer le
  pool decentralisé sur une autre machine et la connecter à ce noeud Monero

## Support

Je ne suis pas dévellopeur, n'ai aucune formation de code, je suis simplement
autodidact.
Si vous avez une question concernant HA et ses add-ons vous pouvez consulter:

- [Le Forum communautaire francophone][hacf] de HomeAssistant
- [Le Forum communautaire anglophone][forum] de HomeAssistant.
- [Le serveur Discord][discord-ha] de HomeAssistant.

## License

MIT License

Copyright (c) 2022-2024 [Frosh][frosh]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

> **_Parts of the project are originally Copyright (c) 2014-2023, [The Monero Project][themoneroproject],
> distributed under [licence][monerolicense]:_**
>
> Redistribution and use in source and binary forms, with or without modification,
> are permitted provided that the following conditions are met:
>
> > _1. Redistributions of source code must retain the above copyright notice, this
> > list of conditions and the following disclaimer._
> >
> > _2. Redistributions in binary form must reproduce the above copyright notice,
> > this list of conditions and the following disclaimer in the documentation and/or
> > other materials provided with the distribution._
> >
> > _3. Neither the name of the copyright holder nor the names of its contributors
> > may be used to endorse or promote products derived from this software without
> > specific prior written permission._
> >
> > _THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
> > AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
> > WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
> > DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
> > FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
> > DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
> > SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
> > CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
> > OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
> > OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE._

[add-addon]: https://my.home-assistant.io/redirect/supervisor_addon/?addon=c751e21a_monerod
[add-addon-shield]: https://my.home-assistant.io/badges/supervisor_addon.svg
[add-repo]: https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A//github.com/erdnaxela02/hassio-addons
[add-repo-shield]: https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg
[releases]: https://github.com/erdnaxela02/addon-monerod/releases
[releases-shield]: https://img.shields.io/github/v/release/erdnaxela02/addon-monerod
[license-shield]: https://img.shields.io/github/license/erdnaxela02/addon-monerod
[aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[getmonero]: https://www.getmonero.org
[pruning]: https://www.getmonero.org/resources/moneropedia/pruning.html
[addon_p2pool]: https://github.com/erdnaxela02/addon-p2pool
[p2pool]: https://github.com/SChernykh/p2pool
[discord-ha]: https://discord.gg/c5DvZ4e
[forum]: https://community.home-assistant.io
[hacf]: https://forum.hacf.fr/
[frosh]: https://github.com/erdnaxela02
[themoneroproject]: https://github.com/monero-project
[monerolicense]: https://github.com/monero-project/monero/blob/master/LICENSE
