BanishedTranslationTH
=====================
ส่วนสเริมภาษาไทยสำหรับเกม [Banished โดย Shinning Rock Software](http://www.shiningrocksoftware.com/)
This is a Thai language translation mod repository for the game [Banished by Shinning Rock Software](http://www.shiningrocksoftware.com/).

Download
========
สำหรับเกมเมอร์ คุณสามารถดาวน์โหลดอัพเดทล่าสุดได้จากหน้า [Release](https://github.com/iAmMutun/BanishedTranslationTH/releases)
For normal gamers, you can download the latest release or older releases on the [Release](https://github.com/iAmMutun/BanishedTranslationTH/releases) page.

Contribute
==========
First of all, the current Thai font used in the translation is **TH Bai Jamjuree CP (TH Baijam)**. Get it from [f0nt.com](http://www.f0nt.com/release/13-free-fonts-from-sipa/) and install it on your PC.

Next, you need to properly set up the [**Banished Mod Kit** build 160521](http://www.shiningrocksoftware.com/2016-05-22-quick-fixes/), older or newer version may not work properly. Install all the prerequisites, _except_ the graphics SDKs, they're huge, we're just translating the game, not modding the graphics. Also, study the translation example from `README.html` in the mod kit or [from the developer's blog](http://www.shiningrocksoftware.com/mods/), because I'm not going to explain about the translation process, only how to use the tools for doing it in Thai language more easily.

Once the mod kit is installed, clone this repository in to the mod kit directory, and you're almost ready. But before you can help translate Banished into Thai, be noted, certain Thai characters commonly tend to have rendering issues in many programs and games, including Banished. The notably issues are the floating tone markers and overlapping vowels. We will discuss about that in a bit. For now, just remember that when you need to introduce Thai characters in any *.rsc* files, you have to move them inside `TH` folder and preserve the directory as if the`TH` folder was another mod folder. Also, save the file in UTF-8 format. Either with or without byte order mark (BOM) will work.

Now you're ready to do some translations! Just edit those *.rsc* files.

To build the Thai translation mod, simply run the `Build.bat` script. This will create several files and folder in our directory, and also the `translationThai.pkm` file in `bin/WinData` folder under mod kit directory. If you've already build the mod before, you may also want to run `Clean.bat` to clean up older files to avoid unintended left-over changes.

By default, when you run the `Build.bat`, the `UnicodeFix64.exe` or `UnicodeFix32.exe` will be called. [This is a small program I wrote](https://github.com/iAmMutun/BanishedTHUnicodeFix) to help us fix the problem with Thai language, as mentioned earlier. It'll change the Unicode of those problematic characters to the more appropriate one, based on their surrounding characters. Any *.rsc* files inside `TH` folder will be read then a fixed, UTF-16 converted file will be created at the corresponding path.

Finally, you can check out the result using the executable files shipped with the mod kit by running `TestRun.bat`.

Happy translating! :)
