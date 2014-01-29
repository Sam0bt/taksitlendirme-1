<?php
function taksitHesap($taksit,$para){
	$dizi 	 = array();
	$date    = date('d-m-Y');  
	for ($sayac = 1; $sayac <= $taksit ; $sayac++ ) {
		@$dizi['taksitSayisi'] 	.= $sayac;
		@$dizi['taksitPara']	.= round($para/$sayac,2);
		@$dizi['taksitTarih']	.= date( "d-m-Y", strtotime("$date,+$sayac month")).'<br>';
	}
    return $dizi;
}  
	$taksitArray = taksitHesap(12,1000);
	$taksitSayi	 = $taksitArray["taksitSayisi"];
	$taksitPara	 = $taksitArray["taksitPara"];
	$taksitTarih = $taksitArray["taksitTarih"];
	echo '
		<table class="table span8 kapsa">
				<thead>
					<tr>
						<th>Taksit Sayısı</th>
						<th>Aylık Taksit Miktarı</th>
						<th>Aylık Taksit Tarihleri</th>
					</tr>
				</thead>
				<tbody>
	';

			/*
			foreach($taksitSayi as $taksitSayisi){
				foreach($taksitPara as $taksitParasi){
					foreach($taksitTarih as $taksitTarihi){
						echo '
							<tr>
								<td>'.$taksitSayisi.'</td>
								<td>'.$taksitParasi.'</td>
								<td>'.$taksitTarihi.'</td>
							</tr>
						';
					}
				}
			}*/
	#Foreach kullandığımda Invalid argument supplied for foreach() hatası alıyorum
	$taksitSayiCount	=	count($taksitSayi);
	$taksitParaCount	=	count($taksitPara);
	$taksitTarihCount	=	count($taksitTarih);
				for($x=0;$x<$taksitSayiCount;$x++){
					for($y=0;$y<$taksitParaCount;$y++){
						for($z=0;$z<$taksitTarihCount;$z++){
							echo '
							<tr>
								<td>'.$taksitSayi[$x].'</td>
								<td>'.$taksitPara[$y].'</td>
								<td>'.$taksitTarih[$z].'</td>
							</tr>
							';
						}
					}
				}
				#for kullandığımda da olmuyor
			
			
	echo '
				</tbody>
		</table>
	';
?>
