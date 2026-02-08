[Persistent Store service](https://github.com/kinnay/NintendoClients/wiki/Persistent-Store-Protocol) is a standard Quazal protocol for remote file storage. ACB's multiplayer binary fetches a ~60KB `.cxb` binary file with game settings. The file stores plain text, pure binary data and malformed XML data. The format is unknown and a settings file is served as-seen as of July 23rd, 2023.

An example file is [gamesettings_c1380_d873_s6285.cxb](uploads/2574457c34d5dab2e28a11dc54817aab/gamesettings_c1380_d873_s6285.cxb), hardcoded in the MP binary. It may be unique per game copy.
