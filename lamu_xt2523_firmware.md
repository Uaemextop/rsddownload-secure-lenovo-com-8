# Firmware / ROMs para lamu · lamuc · lamug (XT2523)

Extraído de `lmsa_firmware_urls.txt` y `download_links.txt`.

> **Nota sobre ROMs de ingeniería:** No se encontraron builds de tipo `eng` o `userdebug`
> en los archivos analizados. Todos los paquetes disponibles son builds de producción
> (`user` / `release-keys`).

---

## lamu — variante global (XT2523)

| Archivo | Android | Build | URL |
|---------|---------|-------|-----|
| `fastboot_lamu_g_user_15_VVTAS35.51-137-2_f1c510_release-keys.zip` | 15 | VVTAS35.51-137-2 | https://rsddownload-secure.lenovo.com/fastboot_lamu_g_user_15_VVTAS35.51-137-2_f1c510_release-keys.zip |
| `fastboot_lamu_g_user_15_VVTA35.51-137-10_cabf9d_release-keys.zip` | 15 | VVTA35.51-137-10 | https://rsddownload-secure.lenovo.com/fastboot_lamu_g_user_15_VVTA35.51-137-10_cabf9d_release-keys.zip |
| `fastboot_lamu_g_user_15_VVTAS35.51-137-2-1_c99c2a_release-keys.zip` | 15 | VVTAS35.51-137-2-1 | https://rsddownload-secure.lenovo.com/fastboot_lamu_g_user_15_VVTAS35.51-137-2-1_c99c2a_release-keys.zip |

---

## lamuc — variante China/UC (XT2523)

| Archivo | Android | Build | URL |
|---------|---------|-------|-----|
| `fastboot_lamuc_g_user_15_VVTB35.41-41_93e397_release-keys.zip` | 15 | VVTB35.41-41 | https://rsddownload-secure.lenovo.com/fastboot_lamuc_g_user_15_VVTB35.41-41_93e397_release-keys.zip |
| `fastboot_lamuc_g_user_15_VVTB35.41-47_6eb4a4_release-keys.zip` | 15 | VVTB35.41-47 | https://rsddownload-secure.lenovo.com/fastboot_lamuc_g_user_15_VVTB35.41-47_6eb4a4_release-keys.zip |
| `fastboot_lamuc_g_user_15_VVTB35.41-41_93e397_release-keys_elabel_XT2623-2_demogb.zip` | 15 | VVTB35.41-41 (demo GB, elabel XT2623-2) ¹ | https://rsddownload-secure.lenovo.com/fastboot_lamuc_g_user_15_VVTB35.41-41_93e397_release-keys_elabel_XT2623-2_demogb.zip |

> ¹ Este paquete comparte el codename `lamuc` pero el sufijo `_elabel_XT2623-2_demogb`
> indica que la sobreposición de etiqueta electrónica es para el modelo **XT2623-2**
> (distinto del XT2523). Puede ser aplicable a unidades de demostración con ese número de modelo.

---

## lamulg — variante LATAM global (XT2523)

| Archivo | Android | Build | URL |
|---------|---------|-------|-----|
| `fastboot_lamulg_g_user_14_UUTBS34.40-41-3_40-41-3_release-keys_FLASH_sign_20260129204648.zip` | 14 | UUTBS34.40-41-3 | https://moto-rsd-prod-secure.s3.dualstack.us-east-1.amazonaws.com/fastboot_lamulg_g_user_14_UUTBS34.40-41-3_40-41-3_release-keys_FLASH_sign_20260129204648.zip |

---

## Cómo flashear (fastboot)

Estos paquetes son **fastboot ROM** estándar de Motorola/Lenovo. Procedimiento general:

```bash
# 1. Descomprimir el zip
unzip fastboot_lamu_g_user_15_*.zip

# 2. Arrancar en fastboot
adb reboot bootloader

# 3. Flashear con el script incluido (Windows)
flash-all.bat

# 3. O en Linux/macOS
./flash-all.sh
```

> ⚠️ Requiere bootloader desbloqueado. El proceso borra todos los datos del dispositivo.
