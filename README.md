# FixNfc

Fixes NFC on **Xiaomi sapphire** (Redmi Note 13 4G / Redmi Note 13 4G NFC) when building a custom Android ROM.

Run it on your PC against your ROM source. It does not run on the phone.

## Before you start

You need **Linux or WSL** and **Python 3**. The script is written in bash, but it uses Python 3 internally to edit the ROM files.

Check if Python 3 is installed:

```bash
python3 --version
```

If you get "command not found", install it:

```bash
sudo apt install python3
```

## How to use

**1. Download the script**

```bash
git clone https://github.com/WibuRachSapphireTree/FixNFC.git
```

**2. Go into the folder**

```bash
cd FixNFC
```

**3. Allow the script to run**

```bash
chmod +x FixNFC.sh
```

**4. Run it on your ROM source**

```bash
./FixNFC.sh ~/aosp
```

Replace `~/aosp` with the path to your ROM source folder.

**5. Rebuild your ROM**

Build as usual, then flash.

## Optional

Preview the changes without modifying anything:

```bash
./FixNFC.sh --check ~/aosp
```

## Notes

- Safe to run more than once.
- Do not use `sudo` to run the script.
- It edits files in your source, so back it up or commit first.

## Errors

**`Permission denied`**: run step 3 again.

**`Khong tim thay thu muc`**: the source path is wrong.

**`Khong tim thay day du tep can thiet`**: that folder is not your ROM source root.

**`Can cai python3`**: install Python 3 (see "Before you start").
