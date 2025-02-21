# Sumatif
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sumatif Individu</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 20px; padding: 20px; }
        .hidden { display: none; }
        label { display: block; margin: 10px 0 5px; }
        button { margin-top: 15px; padding: 10px; }
    </style>
</head>
<body>
    <h2>Sumatif Individu Teknologi Digital</h2>
    
    <div id="startSection">
        <label for="name">Masukkan Nama Anda:</label>
        <input type="text" id="name" required>
        <button onclick="startTest()">Mulai Tes</button>
    </div>

    <div id="testSection" class="hidden">
        <h3>Soal Pilihan Ganda</h3><br>
	<h4><b>Setiap soal bernilai 5 poin</b></h4>
        <form id="testForm">
            <ol>
                <li>
                    <p>'Bilangan heksadesimal C5 dalam bilangan biner adalah...</p>
                    <label><input type="radio" name="q1" value="10110101"> 10110101</label>
                    <label><input type="radio" name="q1" value="11001010"> 11001010</label>
                    <label><input type="radio" name="q1" value="11000101"> 11000101</label>
                </li>
                <li>
                    <p>Teknologi nirkabel yang menggunakan gelombang radio untuk komunikasi jarak pendek adalah...</p>
                    <label><input type="radio" name="q2" value="Bluetooth"> Bluetooth</label>
                    <label><input type="radio" name="q2" value="Wi-Fi"> Wi-Fi</label>
                    <label><input type="radio" name="q2" value="Seluler"> Seluler</label>
                </li>
 		<li>
                    <p>Jenis kabel yang umum digunakan dalam jaringan Ethernet adalah...</p>
                    <label><input type="radio" name="q3" value="Pilin"> Pilin</label>
                    <label><input type="radio" name="q3" value="Koaksial"> Koaksial</label>
                    <label><input type="radio" name="q3" value="Serat optik"> Serat optik</label>
                </li>
		<li>
                    <p>Bilangan oktal 52 dalam bilangan biner adalah...</p>
                    <label><input type="radio" name="q4" value="101100"> 101100</label>
                    <label><input type="radio" name="q4" value="101010"> 101010</label>
                    <label><input type="radio" name="q4" value="110010"> 110010</label>
                </li>
		<li>
                    <p>Terjemahkan kode binner berikut: 01010010  01100001  01101010  01101001  01101110</p>
                    <label><input type="radio" name="q5" value="Kasih"> Kasih</label>
                    <label><input type="radio" name="q5" value="Tekun"> Tekun</label>
                    <label><input type="radio" name="q5" value="Rajin"> Rajin</label>
                </li>
		<li>
                    <p>Layanan penyimpanan data yang menggunakan internet disebut...</p>
                    <label><input type="radio" name="q6" value="Cloud storage"> Cloud storage</label>
                    <label><input type="radio" name="q6" value="Harddisk"> Harddisk</label>
                    <label><input type="radio" name="q6" value="Compact Disk"> Compact Disk</label>
                </li>
		<li>
                    <p>Jenis penyimpanan data yang menggunakan teknologi magnetik adalah...</p>
                    <label><input type="radio" name="q7" value="Compact Disk"> Compact Disk</label>
                    <label><input type="radio" name="q7" value="Harddisk"> Harddisk</label>
                    <label><input type="radio" name="q7" value="Cloud Storage"> Cloud Storage</label>
                </li>
		<li>
                    <p>Gerbang logika yang menghasilkan output 1 hanya jika inputnya sama adalah...</p>
                    <label><input type="radio" name="q8" value="EX-OR"> EX-OR</label>
                    <label><input type="radio" name="q8" value="EX-NOR"> EX-NOR</label>
                    <label><input type="radio" name="q8" value="OR"> OR</label>
                </li>
		<li>
                    <p>Gerbang logika yang menghasilkan output 0 jika salah satu inputnya 1 adalah...</p>
                    <label><input type="radio" name="q9" value="NOR">NOR</label>
                    <label><input type="radio" name="q9" value="EX-NOR">EX-NOR</label>
                    <label><input type="radio" name="q9" value="NOT">NOT</label>
                </li>
		<li>
                    <p>Gerbang logika yang hanya memiliki 1 input dan 1 output adalah...</p>
                    <label><input type="radio" name="q10" value="NOT"> NOT</label>
                    <label><input type="radio" name="q10" value="AND"> AND</label>
                    <label><input type="radio" name="q10" value="OR"> OR</label>
                </li>
		            </ol>
                    <br><br>
                    
            <h3>Soal Esai</h3><br>
		<h4><b>Setiap soal bernilai 10 poin</b></h4>
                <ol>
                <li><label>Apa yang dimaksud dengan media penyimpanan data?</label><textarea name="essay1" cols="100" rows="10"></textarea></li>
                <li><label>Berapa hasil konversi bilangan biner 1011 ke desimal?</label><textarea name="essay2" cols="100" rows="10"></textarea></li>
		        <li><label>Sebutkan 3 keunggulan cloud storage dibandingkan media penyimpanan yang lain!</label><textarea name="essay3" cols="100" rows="10"></textarea></li>
                <li><label>Jelaskan pemahamanmu mengenai dua gerbang logika!</label><textarea name="essay4" cols="100" rows="10"></textarea></li>
                <li><label>Terjemahkan bilangan binner berikut: 01001011  01100001  01110011  01101001  01101000"</label><textarea name="essay5" cols="100" rows="10"></textarea></li>
            </ol>
                        <button type="submit">Kirim Jawaban</button>
        </form>
    </div>

    <script>
        let isTestActive = false;

        function startTest() {
            const name = document.getElementById("name").value.trim();
            if (name === "") {
                alert("Harap masukkan nama Anda!");
                return;
            }
            sessionStorage.setItem("testActive", "true");
            sessionStorage.setItem("userName", name);

            document.getElementById("startSection").classList.add("hidden");
            document.getElementById("testSection").classList.remove("hidden");
            isTestActive = true;
        }

        function checkFocus() {
            if (isTestActive && document.hidden) {
                alert("Anda keluar dari tab! Tes akan direset.");
                sessionStorage.removeItem("testActive");
                location.reload();
            }
        }

        document.addEventListener("visibilitychange", checkFocus);

        document.getElementById("testForm").addEventListener("submit", function(event) {
            event.preventDefault();

            let formData = new FormData(this);
            formData.append("name", sessionStorage.getItem("userName"));

            let formObj = {};
            formData.forEach((value, key) => { formObj[key] = value; });

            fetch("https://prod-02.southeastasia.logic.azure.com:443/workflows/67e794d407d7497fa06b40f43a5e3c62/triggers/manual/paths/invoke?api-version=2016-06-01&sp=%2Ftriggers%2Fmanual%2Frun&sv=1.0&sig=5YBP8YKtHlRsAVAVokqu7DYkAKmKNsQO9Us03SR-cek", {
                method: "POST",
                headers: { "Content-Type": "application/json" },
                body: JSON.stringify(formObj)
            }).then(response => {
                if (response.ok) {
                    alert("Tes berhasil dikirim!");
                    sessionStorage.removeItem("testActive");
                    location.reload();
                } else {
                    alert("Gagal mengirim tes. Periksa koneksi internet Anda.");
                }
            }).catch(error => {
                alert("Terjadi kesalahan: " + error);
            });
        });
    </script>
</body>
</html>
