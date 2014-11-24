Alsa-Mixer
==========
Alsa-Mixer is a gnome-shell extension to control ALSA output (Master) volume.

<h3> Installation </h3>
run install.sh (recommended)
<pre>
git clone git://github.com/texasflood/Alsa-Mixer.git Alsa-Mixer
cd Alsa-Mixer
chmod +x install.sh
./install.sh
</pre>
or detailed installation
<pre>
git clone git://github.com/texasflood/Alsa-Mixer.git Alsa-Mixer
mkdir -p ~/.local/share/gnome-shell/extensions/alsaVolbar\@texasflood.github.com
cp Alsa-Mixer/extension.js ~/.local/share/gnome-shell/extensions/alsaVolbar\@texasflood.github.com
cp Alsa-Mixer/metadata.json ~/.local/share/gnome-shell/extensions/alsaVolbar\@texasflood.github.com
rm -rf Alsa-Mixer/
</pre>

This is an updated version with a bug fix, the original code was written by Victor Aurélio Santos.
The bug fix is related to a corner case, when the volume reaches 100%, the extension crashes as the regular expression does not handle three digits. In normal use, when the volume reaches 100%, the volume controller crashes. I have also added a simple mute detector.

To mute/unmute without closing the menu, toggle the Sound switch with the spacebar.

License GPLv3
