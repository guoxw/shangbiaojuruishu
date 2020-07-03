# shangbiaojuruishu
商标局瑞数绕过与爬取分析

贴逆向好的js代码..剩下靠你们自己了

需要返回cookie,否则无限跳转,下面是nginx静态服务配置

	# nginx配置
	server {
        listen       801;
        server_name  wcjs.sbj.cnipa.gov.cn;

		
		
        #charset koi8-r;

        #access_log  logs/host.access.log  main;
		
		
		# 自定义的静态文件
		location ~ ^/111/ {
            root html/wcjs.sbj.cnipa.gov.cn/;

        }
		
		location  = / {
			root html/wcjs.sbj.cnipa.gov.cn/;
			index index.html;
			
			add_header 'Set-Cookie' 'o3KxeTTl0htJS=50uYHOItIb7oIqbA5HfPI8hMnrkQF.ubLhW13hxZ7hdAVpuhE8u14AoVYz1IV1t2VT387YEm.gtbKyFNwlNVacA; Path=/; expires=Sat, 13 Apr 2030 08:01:56 GMT; HttpOnly';
			add_header 'Set-Cookie' '__jsluid_h=ec57e7f8c18fce25ac47b018753c92ae; max-age=31536000; path=/; HttpOnly';
			
        }
		
		location / {
			root html/wcjs.sbj.cnipa.gov.cn/;
			index index.html;
			
        }
	}



2605326000@qq.com
