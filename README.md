<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form Outbound</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f0f0;
        }
        .container {
            max-width: 600px;
            margin: 20px auto;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 10px;
            background-color: #fff;
        }
        h2 {
            text-align: center;
            color: #333;
        }
        .form-group {
            margin-bottom: 20px;
        }
        .form-group label {
            font-weight: bold;
            display: block;
            color: #333;
        }
        .form-group input, .form-group select {
            width: 100%;
            padding: 10px;
            margin-top: 5px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .form-group button {
            width: 100%;
            padding: 12px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            cursor: pointer;
        }
        .form-group button:hover {
            background-color: #45a049;
        }
        #other-armada, #other-plat {
            display: none;
        }
        /* Responsiveness */
        @media (max-width: 600px) {
            .container {
                padding: 15px;
            }
            .form-group input, .form-group select, .form-group button {
                padding: 12px;
            }
        }
        /* Loading Indicator */
        #loading {
            display: none;
            text-align: center;
            margin-top: 20px;
            font-size: 18px;
            color: #333;
        }
    </style>
</head>
<body>

<div class="container">
    <h2>Form Outbound</h2>
    <form action="URL_WEB_APP_ANDA" method="post" enctype="multipart/form-data">
        <div class="form-group">
            <label for="armada">Armada</label>
            <select id="armada" name="armada" required>
                <option value="">Pilih Armada</option>
                <option value="Inhouse">Inhouse</option>
                <option value="Delivere">Delivere</option>
                <option value="Pickup Customer">Pickup Customer</option>
                <option value="Pickup Angkutan">Pickup Angkutan</option>
                <option value="Lainnya">Lainnya</option>
            </select>
        </div>
        <div class="form-group">
            <label for="drop-point">Drop Point Total</label>
            <input type="number" id="drop-point" name="drop_point" required>
        </div>
        <div class="form-group">
            <label for="qty">Qty</label>
            <input type="number" id="qty" name="qty" required>
            <span>KG</span> <!-- Menambahkan satuan KG -->
        </div>
        <div class="form-group">
            <label for="driver">Driver</label>
            <select id="driver" name="driver" required>
                <option value="">Pilih Driver</option>
                <option value="Syafe'i">Syafe'i</option>
                <option value="Tajwini">Tajwini</option>
                <option value="Karis">Karis</option>
                <option value="Sunari">Sunari</option>
                <option value="Hayatami">Hayatami</option>
                <option value="Rohani">Rohani</option>
                <option value="Sidik">Sidik</option>
                <option value="Kusnadi">Kusnadi</option>
                <option value="M. Zarkasih">M. Zarkasih</option>
                <option value="Idris">Idris</option>
                <option value="Via Agkutan">Via Agkutan</option>
                <option value="Pickup">Pickup</option>
                <option value="Leider">Leider</option>
                <option value="Hamdori">Hamdori</option>
                <option value="Deliveree">Deliveree</option>
            </select>
        </div>
        <div class="form-group">
            <label for="plat-kendaraan">Plat Kendaraan</label>
            <select id="plat-kendaraan" name="plat_kendaraan" required>
                <option value="">Pilih Plat Kendaraan</option>
                <option value="B 9041 FEN">B 9041 FEN - Fuso 10 Ton</option>
                <option value="B 9303 CCF">B 9303 CCF - L 300 2 Ton</option>
                <option value="B 9448 FCL">B 9448 FCL - Double 5 ton</option>
                <option value="B 9489 FCD">B 9489 FCD - Fuso 10 Ton</option>
                <option value="B 9649 FCL">B 9649 FCL - Double 5 ton</option>
                <option value="B 9715 CRX">B 9715 CRX - Fuso 10 Ton</option>
                <option value="B 9836 CCF">B 9836 CCF - Double 5 ton</option>
                <option value="B 9925 UCE">B 9925 UCE - Engkel 3 Ton</option>
                <option value="B 9941 FCD">B 9941 FCD - Engkel 3 Ton</option>
                <option value="Via Agkutan">Via Agkutan</option>
                <option value="Pickup">Pickup</option>
                <option value="B 9043 CQA">B 9043 CQA - TANKI</option>
                <option value="Lainnya">Lainnya</option>
            </select>
        </div>
        <div class="form-group">
            <label for="camera">Ambil Foto Kendaraan</label>
            <input type="file" id="camera" name="camera" accept="image/*" capture="camera" required>
        </div>
        <div class="form-group">
            <button type="submit">Kirim</button>
        </div>
    </form>

    <!-- Loading Indicator -->
    <div id="loading">Sedang mengirim...</div>
</div>

</body>
</html>
