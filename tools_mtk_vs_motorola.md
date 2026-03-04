# Herramientas de Flash: MTK SP Flash Tool vs Motorola (LMSA / RSD)

Basado en el análisis de `lmsa_firmware_urls.txt` y `download_links.txt`.

---

## Resumen comparativo de herramientas

| Herramienta | Fabricante | Chipsets | Tipo de paquete en el repositorio | Plataforma |
|-------------|-----------|----------|----------------------------------|------------|
| **SP Flash Tool** | MediaTek | MTK (MT6xxx, MT8xxx) | `_BMP.zip`, `_DL_user_*.zip`, `_MTK_*.zip` | Windows / Linux |
| **QPST** (Qualcomm Product Support Tools) | Qualcomm | QCom (MSM, SDxxx) | `_qpst.zip`, `_qpst.7z` | Windows |
| **QFIL** (Qualcomm Flash Image Loader) | Qualcomm | QCom (EDL/9008) | `_Qfil.zip` | Windows |
| **RSD Lite / RSD Downloader** | Motorola | Qualcomm (Moto) | `_CFC.xml.zip`, `_CFC.zip` | Windows |
| **LMSA** (Rescue & Smart Assistant) | Lenovo/Motorola | Todos (usa RSD backend) | `fastboot_*.zip`, `*_SVC*.zip`, `*_FLASHER_sign_*.zip`, `*_FLASH_sign_*.zip` | Windows / Android |
| **fastboot** | Android/AOSP | Qualcomm, MTK, Unisoc | `fastboot_*.zip` | Windows / Linux / macOS |
| **ImageLoader** | Lenovo | MTK (tablets) | `*_ImageLoader.zip` | Windows (vía LMSA) |

---

## 1. MTK SP Flash Tool — paquetes encontrados

### ¿Qué es?
**SP Flash Tool** (Smart Phone Flash Tool) de MediaTek es la herramienta de flash
para dispositivos con chipset MediaTek. Trabaja con un **Download Agent (DA)** y un
archivo **scatter** incluido dentro del ZIP de firmware.

### Indicadores de paquetes MTK en los archivos TXT

| Sufijo / patrón | Significado |
|-----------------|-------------|
| `_BMP.zip` | Batch Mode Procedure — flash completo vía SP Flash Tool |
| `_DL_user_*.zip` | Download Agent format — SP Flash Tool en modo DL |
| `_MTK_*.zip` | Indicado explícitamente como chipset MTK |
| `mt8167s_*.zip` | Nombre de chipset MTK en el nombre de archivo |
| `M6762_*.zip` | Chipset MT6762 (Helio A22) |

### Paquetes `_BMP` — Tablets Lenovo (SP Flash Tool)

Estos 23 paquetes son para **tabletas Lenovo** con chipset MediaTek y requieren
**SP Flash Tool** para ser flasheados:

| Archivo | Dispositivo | URL |
|---------|-------------|-----|
| `TB-8505X_S110040_210105_BMP.zip` | Lenovo Tab M8 (TB-8505X) | https://moto-rsd-prod-secure.s3.us-east-1.amazonaws.com/TB-8505X_S110040_210105_BMP.zip |
| `TB-8505F_S301002_210730_BMP.zip` | Lenovo Tab M8 FHD (TB-8505F) | https://moto-rsd-prod-secure.s3.us-east-1.amazonaws.com/TB-8505F_S301002_210730_BMP.zip |
| `TB-8705F_S300111_220228_BMP.zip` | Lenovo Tab M8 HD Gen2 (TB-8705F) | https://moto-rsd-prod-secure.s3.us-east-1.amazonaws.com/TB-8705F_S300111_220228_BMP.zip |
| `TB-8705X_S300259_220301_BMP.zip` | Lenovo Tab M8 HD Gen2 (TB-8705X) | https://moto-rsd-prod-secure.s3.us-east-1.amazonaws.com/TB-8705X_S300259_220301_BMP.zip |
| `TB-X606V_S300665_220630_BMP.zip` | Lenovo Tab M10 FHD Plus (TB-X606V) | https://moto-rsd-prod-secure.s3.us-east-1.amazonaws.com/TB-X606V_S300665_220630_BMP.zip |
| `TB-8505F_S320019_220720_BMP.zip` | TB-8505F (actualización) | https://moto-rsd-prod-secure.s3.us-east-1.amazonaws.com/TB-8505F_S320019_220720_BMP.zip |
| `TB-8505X_S320034_221221_BMP.zip` | TB-8505X (actualización) | https://moto-rsd-prod-secure.s3.us-east-1.amazonaws.com/TB-8505X_S320034_221221_BMP.zip |
| `TB-X306F_S120637_230301_BMP.zip` | Lenovo Tab M10 (3rd Gen, TB-X306F) | https://moto-rsd-prod-secure.s3.us-east-1.amazonaws.com/TB-X306F_S120637_230301_BMP.zip |
| `TB-X306X_S120712_230301_BMP.zip` | Lenovo Tab M10 (3rd Gen, TB-X306X) | https://moto-rsd-prod-secure.s3.us-east-1.amazonaws.com/TB-X306X_S120712_230301_BMP.zip |
| `TB-X306XA_S120298_230331_BMP.zip` | TB-X306XA | https://moto-rsd-prod-secure.s3.us-east-1.amazonaws.com/TB-X306XA_S120298_230331_BMP.zip |
| `TB-X306FA_S120300_230331_BMP.zip` | TB-X306FA | https://moto-rsd-prod-secure.s3.us-east-1.amazonaws.com/TB-X306FA_S120300_230331_BMP.zip |
| `TB-8505FS_S301107_230914_BMP.zip` | TB-8505FS | https://moto-rsd-prod-secure.s3.us-east-1.amazonaws.com/TB-8505FS_S301107_230914_BMP.zip |
| `TB-8505XS_S301077_230914_BMP.zip` | TB-8505XS | https://moto-rsd-prod-secure.s3.us-east-1.amazonaws.com/TB-8505XS_S301077_230914_BMP.zip |
| `TB-8505F_S301106_230914_BMP.zip` | TB-8505F (actualización) | https://moto-rsd-prod-secure.s3.us-east-1.amazonaws.com/TB-8505F_S301106_230914_BMP.zip |
| `TB-X606X_S301085_230919_BMP.zip` | TB-X606X | https://moto-rsd-prod-secure.s3.us-east-1.amazonaws.com/TB-X606X_S301085_230919_BMP.zip |
| `TB-X606F_S301068_230919_BMP.zip` | TB-X606F | https://moto-rsd-prod-secure.s3.us-east-1.amazonaws.com/TB-X606F_S301068_230919_BMP.zip |
| `TB-X606FA_S300623_230730_BMP.zip` | TB-X606FA | https://moto-rsd-prod-secure.s3.us-east-1.amazonaws.com/TB-X606FA_S300623_230730_BMP.zip |
| `TB-X606XA_S300633_230729_BMP.zip` | TB-X606XA | https://moto-rsd-prod-secure.s3.us-east-1.amazonaws.com/TB-X606XA_S300633_230729_BMP.zip |
| `TB-X306F_S230940_240402_BMP.zip` | TB-X306F (actualización 2024) | https://rsdsecure-cloud.motorola.com/download/TB-X306F_S230940_240402_BMP.zip |
| `TB-X306X_S230973_240402_BMP.zip` | TB-X306X (actualización 2024) | https://rsdsecure-cloud.motorola.com/download/TB-X306X_S230973_240402_BMP.zip |
| `TB-X306X_S221013_210730_BMP.zip` | TB-X306X | https://moto-rsd-prod-secure.s3.us-east-1.amazonaws.com/TB-X306X_S221013_210730_BMP.zip |
| `LAVIETabE8FHD1_S110008_201225_BMP.zip` | NEC LAVIE Tab E8 FHD | https://moto-rsd-prod-secure.s3.us-east-1.amazonaws.com/LAVIETabE8FHD1_S110008_201225_BMP.zip |
| `LAVIETabE8HD1_S110007_201225_BMP.zip` | NEC LAVIE Tab E8 HD | https://moto-rsd-prod-secure.s3.us-east-1.amazonaws.com/LAVIETabE8HD1_S110007_201225_BMP.zip |

### Paquetes `_DL_user` — Lenovo A158L (SP Flash Tool — feature phone MTK)

Estos paquetes pertenecen al **Lenovo A158L**, teléfono básico con chipset MTK,
que se flashea con **SP Flash Tool** usando el Download Agent incluido:

| Archivo | Región/HW | Notas | URL |
|---------|-----------|-------|-----|
| `EMEA_A158L_K000_DS_V1.0B41_DL_user_SVC.zip` | EMEA, DS (Dual SIM) | Flash normal | https://download.lenovo.com/lsa/Rescue/Smartphone/EMEA_A158L_K000_DS_V1.0B41_DL_user_SVC.zip |
| `APAC_A158L_K300_DS_V1.0B44_DL_user_SVC.zip` | APAC, DS | Flash normal | https://download.lenovo.com/lsa/Rescue/Smartphone/APAC_A158L_K300_DS_V1.0B44_DL_user_SVC.zip |
| `APAC_A158L_K300_DS_V1.0B45_svc.zip` | APAC, DS | Versión servicio | https://download.lenovo.com/lsa/Rescue/Smartphone/APAC_A158L_K300_DS_V1.0B45_svc.zip |
| `EMEA_A158L_K100_DS_V1.0B37_DL_user_ForceFlash.zip` | EMEA, DS | **ForceFlash** (fuerza flash aunque sea la misma versión) | https://moto-rsd-prod-secure.s3.us-east-1.amazonaws.com/EMEA_A158L_K100_DS_V1.0B37_DL_user_ForceFlash.zip |
| `EMEA_A158L_K200_SS_V1.0B34_SVC.zip` | EMEA, SS (Single SIM) | Flash normal | https://moto-rsd-prod-secure.s3.us-east-1.amazonaws.com/EMEA_A158L_K200_SS_V1.0B34_SVC.zip |
| `Thailand_A158L_K120_DS_V1.0B05_DL_user_SVC_ForceFlash.zip` | Thailand, DS | **ForceFlash** | https://moto-rsd-prod-secure.s3.us-east-1.amazonaws.com/Thailand_A158L_K120_DS_V1.0B05_DL_user_SVC_ForceFlash.zip |

### Paquetes `_MTK_` explícitos

| Archivo | Dispositivo | Chipset | URL |
|---------|-------------|---------|-----|
| `L38043_ROW_OPEN_USER_M6762_O_MTK_S256_19L03_SVC.zip` | Lenovo L38043 (ZUI) | MT6762 (Helio A22) | https://moto-rsd-prod-secure.s3.us-east-1.amazonaws.com/L38043_ROW_OPEN_USER_M6762_O_MTK_S256_19L03_SVC.zip |
| `CD_17302F_Ver_15.42.1_mt8167s_xl_prod.1.1.0.5813256_SVC1.zip` | Lenovo CD-17302F | MT8167S | https://rsdsecure-cloud.motorola.com/download/CD_17302F_Ver_15.42.1_mt8167s_xl_prod.1.1.0.5813256_SVC1.zip |

### Cómo usar SP Flash Tool con estos paquetes

```
1. Descomprimir el ZIP
2. Abrir SP Flash Tool (v5.x para dispositivos Android antiguos, v6.x para nuevos)
3. En "Download" → seleccionar el archivo scatter.txt del firmware
4. Poner el dispositivo en modo BROM:
   - Apagar el teléfono
   - Mantener Vol- presionado al conectar el USB (sin batería en algunos modelos)
5. Click en "Download"
```

> ⚠️ **Modo ForceFlash** (`ForceFlash` en el nombre): Activa la opción
> "Format All + Download" en SP Flash Tool — borra todo y reflashea desde cero.
> Usar solo cuando el dispositivo no arranca.

---

## 2. Motorola — herramientas y paquetes

### ¿Qué herramientas usa Motorola?

Motorola usa **tres herramientas distintas** dependiendo del tipo de paquete:

---

### 2a. RSD Lite (Rescue & Smart Device Lite)
**Herramienta:** `RSD Lite` (versión 4.x–6.x) — solo Windows  
**Paquetes:** `*_CFC.xml.zip` — archivos XML de configuración de flash  
**Total en el repositorio:** 1.773 paquetes  
**¿Qué hace?** Flashea el firmware completo en dispositivos Motorola usando la
interfaz propietaria de Motorola (no fastboot estándar).

Ejemplos de paquetes CFC (muestra representativa):

| Archivo | Dispositivo | URL |
|---------|-------------|-----|
| `ATHENE_NPJ25.93-14.7_cid50_subsidy-IUSMXLA_regulatory-DEFAULT_CFC.xml.zip` | Moto G4 (XT1621) | https://download.lenovo.com/lsa/Rescue/Smartphone/XT1621/ATHENE_NPJ25.93-14.7_cid50_subsidy-IUSMXLA_regulatory-DEFAULT_CFC.xml.zip |
| `HARPIA_MPI24.241-15.3_cid50_subsidy-DEFAULT_regulatory-DEFAULT_CFC.xml.zip` | Moto G Play (XT1609) | https://download.lenovo.com/lsa/Rescue/Smartphone/Judo/HARPIA_MPI24.241-15.3_cid50_subsidy-DEFAULT_regulatory-DEFAULT_CFC.xml.zip |
| `SANDERS_NPSS26.116-64-11_cid50_subsidy-DEFAULT_regulatory-DEFAULT_CFC.xml.zip` | Moto E3 (XT1700) | https://download.lenovo.com/lsa/Rescue/Smartphone/Zach/SANDERS_NPSS26.116-64-11_cid50_subsidy-DEFAULT_regulatory-DEFAULT_CFC.xml.zip |
| `GRIFFIN_CMCC_NCC25.106-26_cid11_subsidy-DEFAULT_regulatory-DEFAULT_CFC.xml.zip` | Moto Z (XT1650 CMCC) | https://download.lenovo.com/lsa/Rescue/Smartphone/XT1650/GRIFFIN_CMCC_NCC25.106-26_cid11_subsidy-DEFAULT_regulatory-DEFAULT_CFC.xml.zip |
| `NASH_RETCN_OCX27.138-29_subsidy-DEFAULT_regulatory-DEFAULT_CFC.xml.zip` | Moto Z2 Force (XT1789) | https://download.lenovo.com/lsa/Rescue/Smartphone/XT1789/NASH_RETCN_OCX27.138-29_subsidy-DEFAULT_regulatory-DEFAULT_CFC.xml.zip |
| `ADDISON_NPNS26.118-22-2-17_cid50_subsidy-DEFAULT_regulatory-DEFAULT_CFC.xml.zip` | Moto Z Play (XT1635) | https://download.lenovo.com/lsa/Rescue/Smartphone/Vertex%20XT1635/ADDISON_NPNS26.118-22-2-17_cid50_subsidy-DEFAULT_regulatory-DEFAULT_CFC.xml.zip |

> 📌 **Nota:** Los archivos CFC.xml contienen instrucciones para RSD Lite sobre
> qué particiones flashear y con qué opciones (format, subsidy, regulatory, etc.).
> El archivo ZIP real del firmware se descarga por separado o está incluido.

---

### 2b. LMSA — Rescue & Smart Assistant
**Herramienta:** `LMSA` (versión para Windows o APK Android) — reemplaza a RSD Lite  
**Paquetes:** `fastboot_*.zip`, `*_FLASHER_sign_*.zip`, `*_FLASH_sign_*.zip`, `*_SVC*.zip`  
**APK disponible:** https://download.lenovo.com/lsa/ma.apk

| Archivo | Tipo | URL |
|---------|------|-----|
| `P352CE_PVT_11.0_64B_CFC_LNV_68-66-3.01-01_FLASHER_sign_20230222060541.zip` | FLASHER (Lenovo Smart Paper) | https://rsddownload-secure.lenovo.com/P352CE_PVT_11.0_64B_CFC_LNV_68-66-3.01-01_FLASHER_sign_20230222060541.zip |
| `P352CE_PVT_11.0_64B_CFC_68-66-4.01-01_FLASHER_sign_20230317023056.zip` | FLASHER | https://rsddownload-secure.lenovo.com/P352CE_PVT_11.0_64B_CFC_68-66-4.01-01_FLASHER_sign_20230317023056.zip |
| `fastboot_lamu_g_user_15_VVTAS35.51-137-2_f1c510_release-keys.zip` | fastboot (lamu) | https://rsddownload-secure.lenovo.com/fastboot_lamu_g_user_15_VVTAS35.51-137-2_f1c510_release-keys.zip |
| `fastboot_cancun_g_oem_user_13_TLB33.78-144-1_*_CFC.zip` | fastboot + CFC (cancun) | https://rsddownload-secure.lenovo.com/fastboot_cancun_g_oem_user_13_TLB33.78-144-1_10200742_release-keys_global_CFC.zip |

---

### 2c. fastboot estándar (Android)
**Herramienta:** `fastboot` (parte de Android SDK Platform Tools)  
**Paquetes:** `fastboot_*.zip` que **no** tienen `_CFC` en el nombre

---

## 3. Herramientas especiales y su diferencia

### Tabla diferencial

| Característica | SP Flash Tool (MTK) | QPST (Qualcomm) | QFIL (Qualcomm) | RSD Lite (Motorola) | LMSA (Lenovo/Moto) | fastboot |
|---------------|---------------------|-----------------|-----------------|--------------------|--------------------|---------|
| **Chipset** | MediaTek | Qualcomm | Qualcomm | Qualcomm (Moto) | Todos | Todos |
| **Modo de conexión** | BROM / Preloader | EDL (9008) / QPST | EDL (9008) | Motorola interface | LMSA / fastboot | Fastboot mode |
| **Requiere BL desbloqueado** | ❌ No | ❌ No | ❌ No | ❌ No | ❌ No (modo SVC) | ✅ Sí |
| **Puede flashear particiones individuales** | ✅ Sí | ✅ Sí | ✅ Sí | ❌ No (solo full) | Limitado | ✅ Sí |
| **Puede bypassear FRP/antirollback** | ⚠️ Según DA | ⚠️ Depende | ⚠️ Depende | ❌ No | ❌ No | ❌ No |
| **Software libre** | ❌ No (oficial MTK) | ❌ No (oficial QCom) | ❌ No (oficial QCom) | ❌ No (oficial Moto) | ❌ No | ✅ Sí (AOSP) |
| **SO requerido** | Windows / Linux | Windows | Windows | Windows | Windows / Android | Win / Lin / Mac |
| **Nivel de riesgo** | Alto (puede brickear) | Alto | Alto | Medio | Bajo | Medio |

### Herramientas especiales encontradas

#### `_ForceFlash` (MTK / Lenovo)
Variante de paquete que fuerza el flash incluso si el dispositivo tiene la misma
versión. Necesario cuando el dispositivo está en bootloop o en modo de emergencia.
- Activa la opción **"Format All + Download"** en SP Flash Tool
- Borra todas las particiones antes de escribir

#### `_FLASHER_sign_` (Lenovo — LMSA modo servicio)
Paquetes firmados digitalmente (`_sign_`) para el programa **LMSA** en modo servicio
(`_FLASHER`). Solo funcionan con credenciales de técnico de servicio Lenovo (LMSA
autenticado).

#### `_BMP` (MTK — Batch Mode Procedure)
Paquetes para SP Flash Tool en **modo batch** (BMP). Permiten flashear en
producción/servicio sin intervención manual. Contienen un script de automatización
junto con el scatter y las imágenes de partición.

#### `ImageLoader` (Lenovo — MTK tablets)
Formato propietario de Lenovo para tabletas MTK. Cargado a través de **LMSA**
(no SP Flash Tool directamente). Lenovo abstrae SP Flash Tool detrás de LMSA
para estos modelos.

| Archivo | URL |
|---------|-----|
| `10FHD1_S100012_210622_ROW_ImageLoader.zip` | https://rsdsecure-cloud.motorola.com/download/10FHD1_S100012_210622_ROW_ImageLoader.zip |
| `801LV_USER_S000086_2109291938_Q00014_JP_ImageLoader.zip` | https://rsdsecure-cloud.motorola.com/download/801LV_USER_S000086_2109291938_Q00014_JP_ImageLoader.zip |

---

## 4. Resumen rápido: ¿qué herramienta usar?

| Tengo este archivo... | Uso esta herramienta |
|-----------------------|---------------------|
| `fastboot_*.zip` (sin `_CFC`) | `fastboot flash` (Android SDK) |
| `fastboot_*_CFC.zip` | LMSA para Windows |
| `*_CFC.xml.zip` | RSD Lite 6.x |
| `*_FLASHER_sign_*.zip` | LMSA en modo servicio |
| `*_FLASH_sign_*.zip` | LMSA en modo servicio |
| `*_BMP.zip` | SP Flash Tool (modo BMP) |
| `*_DL_user_*.zip` | SP Flash Tool (modo Download) |
| `*_MTK_*.zip` o `mt8167_*.zip` | SP Flash Tool |
| `*_qpst.zip` o `*_qpst.7z` | QPST |
| `*_Qfil.zip` | QFIL |
| `*_ImageLoader.zip` | LMSA (carga automática) |
| `ma.apk` | Instalar en Android (Rescue & Smart Assistant) |
