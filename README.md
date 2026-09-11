# Kalibracija kamere

Projekt iz kolegija **Računalni vid**.

## Opis projekta

Cilj projekta je prikazati postupak kalibracije kamere korištenjem
biblioteke **OpenCV** i kalibracijskog uzorka u obliku šahovske ploče.

Kalibracijom se određuju intrinzični i ekstrinzični parametri kamere te
koeficijenti distorzije. Dobiveni parametri koriste se za korekciju
geometrijskih izobličenja slike.

## Korišteni alati

- Python
- OpenCV
- NumPy
- Matplotlib
- Jupyter Notebook

## Podaci

Korišteno je **18 slika** šahovske ploče rezolucije **1280 × 720 piksela**.

Na svakoj slici detektirano je **49 unutarnjih kutova**, odnosno uzorak
veličine **7 × 7**.

Za detekciju kutova korištena je funkcija:

`cv2.findChessboardCornersSB()`

## Kalibracija

Za izračun parametara kamere korištena je funkcija:

`cv2.calibrateCamera()`

Dobivena RMS pogreška kalibracije iznosi:

**0.6482 piksela**

Prosječna reprojekcijska pogreška iznosi:

**0.0904 piksela**

## Korekcija distorzije

Nakon kalibracije provedena je korekcija geometrijskih izobličenja
pomoću funkcije:

`cv2.undistort()`

Originalna i korigirana slika uspoređene su kako bi se prikazao učinak
kalibracije.

## Pokretanje

1. Instalirati potrebne biblioteke:
   - `opencv-python`
   - `numpy`
   - `matplotlib`

2. Otvoriti datoteku `camera_calibration.ipynb` u Jupyter Notebooku.

3. Slike kalibracijskog uzorka postaviti u odgovarajuću mapu.

4. Pokrenuti ćelije notebooka redom.

## Autor

Ivan Živković

Računalni vid, 2026.
