# chapter08
利用QTMainshadow 以及DockWidget 搭框架<br/>
实现光照模型，环境光、漫反射、镜面反射,绘制圆环<br/>
    vec3 light_direction = normalize(light_position - vs_worldpos);<br/>
    vec3 normal = normalize(vs_normal);<br/>
    vec3 half_vector = normalize(light_direction + normalize(vs_worldpos));<br/>
    float diffuse = max(0.0, dot(normal, light_direction));<br/>
    float specular = pow(max(0.0, dot(vs_normal, half_vector)), shininess);<br/>
	  if(diffuse == 0.0)<br/>
		  specular = 0.0;<br/>
    color = color_ambient + diffuse * color_diffuse + specular * color_specular;<br/>
    
    
