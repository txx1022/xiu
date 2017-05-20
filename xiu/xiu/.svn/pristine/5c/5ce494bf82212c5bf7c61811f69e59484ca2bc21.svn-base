//判断是否已登录；
var userID = null;
//初始化购物车信息；
function getUserID(){
	var Llength = localStorage.length;
	var Slength = sessionStorage.length;
	if (Llength != 0) {
		var key = localStorage.key(0)
	}
	if (Slength != 0) {
		var key = sessionStorage.key(0)
	}
	userID = key
}
getUserID()



//更新购物车,使用回调函数，当服务器返回值为1，在提示已加入购物车；
function updatashopcart(userid,goodsid,num,callback){
	$.ajax({
		type:"get",
		url:"http://datainfo.duapp.com/shopdata/updatecar.php",
		data:{
			userID:userid,
			goodsID:goodsid,
			number:num
		},
		async:true,
		success:function(data){
			console.log(data)
			if(callback){
				if (data == 1) {
					callback();
				}
			}
		}
	});
}

