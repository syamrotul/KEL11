<html>
<head>
	<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>
<body>
    <center>
        <h1> Perbandingan Penggunaan Lahan Tahun 2019 - 2023 </h1>
		<h3> SYAMROTUL FAUZIAH | NUR WAHYUNI ZULIANTI | AYU MUSTIKA | </h3>
    </center>
<body>
	<div style="width: 80%; margin: auto;">
        <canvas id="perubahanLahanChart"></canvas>
    </div>
</body>
<script>
// Data perubahan penggunaan lahan
         var dataPerubahanLahan = [
            { jenis: 'Pemukiman Tidak Teratur', pl2019: 5, pl2023: 5 },
            { jenis: 'Pemukiman Teratur', pl2019: 3, pl2023: 5 },
            { jenis: 'Ruang Terbuka Hijau', pl2019: 3, pl2023: 3},
            { jenis: 'Sawah', pl2019: 2, pl2023: 4 },
            { jenis: 'Sungai', pl2019: 2, pl2023: 2 },
            { jenis: 'Kawasan Industri', pl2019: 1, pl2023: 1 },
            { jenis: 'Fasilitas Olahraga', pl2019: 2, pl2023: 1 },
			{ jenis: 'Perdagangan dan Jasa', pl2019: 2, pl2023: 2 },
            // ... tambahkan data lainnya sesuai kebutuhan ...
        ];

        // Inisialisasi chart
        var ctx = document.getElementById('perubahanLahanChart').getContext('2d');
        var perubahanLahanChart = new Chart(ctx, {
            type: 'bar',
            data: {
                labels: dataPerubahanLahan.map(item => item.jenis),
                datasets: [{
                    label: 'PL 2019',
                    backgroundColor: 'rgb(0, 255, 254)',
                    borderColor: 'rgb(0, 0, 0)',
                    borderWidth: 1,
                    data: dataPerubahanLahan.map(item => item.pl2019)
                }, {
                    label: 'PL 2023',
                    backgroundColor: 'rgb(127, 255, 1)',
                    borderColor: 'rgb(0, 0, 0)',
                    borderWidth: 1,
                    data: dataPerubahanLahan.map(item => item.pl2023)
                }]
            },
            options: {
                scales: {
                    y: {
                        beginAtZero: true
                    }
                }
            }
        });
</script>
</html>
