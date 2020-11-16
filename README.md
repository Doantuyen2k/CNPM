# CNPM
Tính tiền điện
﻿<html>
<head>
<title>Tinh Tien Dien</title>
<style>
body {
	font-family:verdana;
}
h1 {
	font-size: x-large;
	font-family:Lucida Handwriting;
	background-color:#ff9933;
	
}
thead {
	valign: center;
	background-color:#FFE4B5;
}
table, th, td {
	
	border-collapse: collapse;
	font-size: 18px;
	background-color:#FFFFCC;
}
tbody {
	border-color: #800000;
}

</style>
</head>
<body>
<div id="wrapper">
<div class="container">
	<form id="tinh-tien-dien">
	<table cellspacing="0" cellpadding="5" align="center">
	<thead>
	<tr>
		<th colspan="2"><h1>TÍNH TIỀN ĐIỆN SINH HOẠT<br>BẬC THANG</h1></th>
	</tr>
	</thead>
	<tbody>
	<tr>
		<td>Chỉ số cũ:</td>
		<td><input type="number" id="chi-so-cu" placeholder="Nhập chỉ số cũ" ></td>
	</tr>
		<td>Chỉ số mới:</td>
		<td><input type="number" id="chi-so-moi" placeholder="Nhập chỉ số mới" ></td>
	</tr>
	<tr>
		<td>Điện năng tiêu thụ:</td>
		<td><input id="tieu-thu" disabled="disabled" ></td>
	</tr>
	<tr>
		<td>Thành tiền:</td>
		<td><input id="thanh-tien" disabled="disabled" ></td>
	</tr>
	<tr>
		<td>Tổng tiền đã có VAT: </td>
		<td><input id="VAT" disabled="disabled" ></td>
	</tr>
	<tr>
		<td colspan="2"><center><input type="button" onClick="ThanhToan()" value="Tính tiền điện">&nbsp;&nbsp;&nbsp;&nbsp;
		<input type="reset" value="Tiếp tục">&nbsp;&nbsp;&nbsp;&nbsp;
		<button onclick="self.close()">Thoát</button></center>
	</tr>
	</tbody>
</table>
</form>
</div>
</div>
<script type="text/javascript">
	function ThanhToan() {
		var chisocu = document.getElementById('chi-so-cu');
		var chisomoi = document.getElementById('chi-so-moi');
		var tieuthu = Number(chisomoi.value) - Number(chisocu.value);
			document.getElementById('tieu-thu').value = tieuthu;
		var tong = tieuthu * 2030;
			document.getElementById('thanh-tien').value = tong;
		var VAT;
		if ( tieuthu < 101 )
 			VAT = tong + tieuthu * 1418;
 		else if ( tieuthu.value < 151 )
 			VAT = tong + tieu * 1622;
 		else if ( tieuthu.value < 201 )
 			VAT = tong + tieuthu * 2044;
 		else if ( tieuthu.value < 301 )
 			VAT = tong + tieuthu * 2210;
 		else if ( tieuthu.value < 401 )
 			VAT = tong + tieuthu * 2361;
 		else
 			VAT = tong + tieuthu * 2420;
		
		document.getElementById('VAT').value = VAT;
}

</script>
</body>
</html>
