 <div id="ruffle"></div>
        <script src="https://unpkg.com/@ruffle-rs/ruffle"></script>
        <script>
            var swfobject = {};

            swfobject.embedSWF = function(url, cont) {
                var ruffle = window.RufflePlayer.newest(),
                    player = ruffle.createPlayer();

                // Append the player to the container and make it fullscreen
                document.getElementById(cont).appendChild(player);
                player.style.width = '100%';
                player.style.height = '100%';

                // Load the SWF file
                player.load({ url: url });

                // Update player size on window resize
                window.addEventListener('resize', function() {
                    player.style.width = '100%';
                    player.style.height = '100%';
                });
            }

            // Embed the SWF file in fullscreen
            swfobject.embedSWF('https://raw.githubusercontent.com/rotemple/facultyforum.github.io/refs/heads/main/VulnerableVideo.swf', 'ruffle');
        </script>
