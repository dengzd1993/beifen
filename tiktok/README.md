tiktok自用 版本21.1.0  代码来源于网络

在[rewrite_local]中添加以下重写

(?<=_region=)CN(?=&) url 307 KR
(?<=&mcc_mnc=)4 url 307 2
^(https?:\/\/(tnc|dm)[\w-]+\.\w+\.com\/.+)(\?)(.+) url 302  $1$3
(?<=\d\/\?\w{7}_\w{4}=)1[6-9]..(?=.?.?&) url 307 17

在[mitm]中添加
hostname = *.tiktokv.com,*.byteoversea.com,*.tik-tokapi.com

换区：在[rewrite_local]中添加下句重写，并将CN改为想看的国家/地区的2位大写英文简写 JP（日本）｜KR（韩国）｜UK（英国）｜US（美国）｜TW（台湾）

(?<=_region=)CN(?=&) url 307 CN

列子
(?<=_region=)CN(?=&) url 307 JP
(?<=_region=)CN(?=&) url 307 KR
(?<=_region=)CN(?=&) url 307 TW
(?<=_region=)CN(?=&) url 307 UK
(?<=_region=)CN(?=&) url 307 US
