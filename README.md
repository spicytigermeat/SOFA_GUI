# LabelMakr 🛋️
A GUI Toolkit for generation of Singing Voice Synthesizer Phoneme-level labels, heavily utilizing SOFA & Whisper.

![image](https://github.com/spicytigermeat/SOFA_GUI/assets/103609620/bd9dcbca-facf-469f-9a09-08fb444c1afb)

Please use the portable version for Windows found [here](https://github.com/spicytigermeat/SOFA_GUI/releases/tag/v003)

# Credits 📰

- SOFA developed by [qiuqiao](https://github.com/qiuqiao/SOFA)
- [tgm_sofa](https://github.com/spicytigermeat/SOFA-Models/releases/tag/v0.0.4) is developed by me, tigermeat (used ver: v004)
- Japanese SOFA model trained by [colstone](https://github.com/colstone/SOFA_Models/releases/tag/JPN-V0.0.2b). The installed version is trimmed to save space. (used ver: v0.0.2)
- Japanese G2p Compiled Version by [CjangCjengh](https://github.com/CjangCjengh/japanese_g2p)

## GUI Translations 🗣️
- English/Japanese: tigermeat
- Traditional Chinese: ArchiVoice
- Indonesian: Koji

# Plans 📝

- Implement automatic label cleanup (using labbu library)
- Clean up code and fix up localization method (i don't like i18n)
- ~Implement support for Japanese model by colstone~ Implemented in v003


# Manual installation 🧰

If you'd like to install this manually, follow these steps!
Requirements:
- anaconda3
- Windows/Linux (Tested on Win11/Ubuntu 22.04 with conda)

Known issues:
- It looks really ugly on Linux (issue with customtkinter being ran on python 3.8, not a priority to fix rn)

1: Create a new environment and activate it, then CD to an empty folder.

Windows:
```
conda create -n sofa_gui python=3.8 -y
conda activate sofa_gui
cd {path_to_folder}
```
Linux:
```
conda create -n sofa_gui python=3.8 -y
source activate sofa_gui
cd {path_to_folder}
```

2: Manually install torch.

Windows:
```
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
```
Linux:
```
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
```

3: Install SOFA_GUI

Windows:
```
git clone https://github.com/spicytigermeat/SOFA_GUI.git
pip install -r requirements.txt
```
Linux:
```
git clone https://github.com/spicytigermeat/SOFA_GUI.git
pip3 install -r requirements.txt
```

4: Install SOFA

Windows:
```
cd SOFA_GUI
git clone https://github.com/qiuqiao/SOFA.git
pip install -r SOFA/requirements.txt
```

Linux:
```
cd SOFA_GUI
git clone https://github.com/qiuqiao/SOFA.git
pip install -r SOFA/requirements.txt
```

5: Manually install the SOFA Model.

Download the files from [this release](https://github.com/spicytigermeat/SOFA-Models/releases/tag/v0.0.4).

Place "tgm_sofa_v004.ckpt" in `SOFA_GUI/SOFA/ckpt`
Place "tgm_sofa_dict.txt" in `SOFA_GUI/SOFA/dictionary`

This should work, please let me know if any steps listed here do not achieve the desired result!

