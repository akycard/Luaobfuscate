local v0=string.char;local v1=string.byte;local v2=string.sub;local v3=bit32 or bit ;local v4=v3.bxor;local v5=table.concat;local v6=table.insert;local function v7(v24,v25) local v26={};for v41=1, #v24 do v6(v26,v0(v4(v1(v2(v24,v41,v41 + 1 )),v1(v2(v25,1 + (v41% #v25) ,1 + (v41% #v25) + 1 )))%256 ));end return v5(v26);end local v8=tonumber;local v9=string.byte;local v10=string.char;local v11=string.sub;local v12=string.gsub;local v13=string.rep;local v14=table.concat;local v15=table.insert;local v16=math.ldexp;local v17=getfenv or function() return _ENV;end ;local v18=setmetatable;local v19=pcall;local v20=select;local v21=unpack or table.unpack ;local v22=tonumber;local function v23(v27,v28,...) local v29=1;local v30;v27=v12(v11(v27,5),v7("\134\133","\173\168\171\23\68\52\157"),function(v42) if (v9(v42,6 -4 )==(97 -(10 + 8))) then v30=v8(v11(v42,1,1));return "";else local v101=v10(v8(v42,49 -33 ));if v30 then local v114=v13(v101,v30);v30=nil;return v114;else return v101;end end end);local function v31(v43,v44,v45) if v45 then local v102=0;local v103;while true do if (v102==0) then v103=(v43/(2^(v44-1)))%(2^(((v45-1) -(v44-1)) + (3 -2))) ;return v103-(v103%1) ;end end else local v104=0;local v105;while true do if (v104==0) then v105=2^(v44-1) ;return (((v43%(v105 + v105))>=v105) and 1) or 0 ;end end end end local function v32() local v46=0;local v47;while true do if (v46==0) then v47=v9(v27,v29,v29);v29=v29 + 1 ;v46=1;end if (v46==1) then return v47;end end end local function v33() local v48,v49=v9(v27,v29,v29 + 2 );v29=v29 + 2 ;return (v49 * 256) + v48 ;end local function v34() local v50,v51,v52,v53=v9(v27,v29,v29 + 3 );v29=v29 + 4 ;return (v53 * 16777216) + (v52 * 65536) + (v51 * 256) + v50 ;end local function v35() local v54=0;local v55;local v56;local v57;local v58;local v59;local v60;while true do if (v54==2) then v59=v31(v56,463 -(416 + 26) ,31);v60=((v31(v56,102 -70 )==1) and  -1) or 1 ;v54=3;end if (v54==1) then v57=1;v58=(v31(v56,1,20) * (2^32)) + v55 ;v54=2;end if (v54==3) then if (v59==0) then if (v58==0) then return v60 * (0 -0) ;else v59=1;v57=0;end elseif (v59==(879 + 1168)) then return ((v58==(0 -0)) and (v60 * (1/0))) or (v60 * NaN) ;end return v16(v60,v59-1023 ) * (v57 + (v58/(2^52))) ;end if (v54==0) then v55=v34();v56=v34();v54=1;end end end local function v36(v61) local v62;if  not v61 then local v106=0;while true do if (v106==0) then v61=v34();if (v61==0) then return "";end break;end end end v62=v11(v27,v29,(v29 + v61) -1 );v29=v29 + v61 ;local v63={};for v77=1, #v62 do v63[v77]=v10(v9(v11(v62,v77,v77)));end return v14(v63);end local v37=v34;local function v38(...) return {...},v20("#",...);end local function v39() local v64={};local v65={};local v66={};local v67={v64,v65,nil,v66};local v68=v34();local v69={};for v79=1,v68 do local v80=0;local v81;local v82;while true do if (1==v80) then if (v81==1) then v82=v32()~=0 ;elseif (v81==2) then v82=v35();elseif (v81==(7 -4)) then v82=v36();end v69[v79]=v82;break;end if (v80==0) then v81=v32();v82=nil;v80=1;end end end v67[622 -(555 + 64) ]=v32();for v83=1,v34() do local v84=v32();if (v31(v84,1,1)==0) then local v110=0;local v111;local v112;local v113;while true do if (1==v110) then v113={v33(),v33(),nil,nil};if (v111==0) then local v121=0;while true do if (v121==0) then v113[3]=v33();v113[4]=v33();break;end end elseif (v111==1) then v113[3]=v34();elseif (v111==2) then v113[3]=v34() -(2^(446 -(44 + 386))) ;elseif (v111==3) then v113[3]=v34() -(2^16) ;v113[4]=v33();end v110=2;end if (v110==0) then v111=v31(v84,2,441 -(145 + 293) );v112=v31(v84,4,6);v110=1;end if (v110==2) then if (v31(v112,1,1487 -(998 + 488) )==1) then v113[2]=v69[v113[2]];end if (v31(v112,570 -(367 + 201) ,2)==1) then v113[3]=v69[v113[3]];end v110=3;end if (v110==3) then if (v31(v112,930 -(214 + 713) ,3)==1) then v113[2 + 2 ]=v69[v113[4]];end v64[v83]=v113;break;end end end end for v85=1,v34() do v65[v85-1 ]=v39();end return v67;end local function v40(v71,v72,v73) local v74=v71[1 + 0 ];local v75=v71[774 -(201 + 571) ];local v76=v71[1 + 2 ];return function(...) local v87=v74;local v88=v75;local v89=v76;local v90=v38;local v91=1;local v92= -(1 + 0);local v93={};local v94={...};local v95=v20("#",...) -(878 -(282 + 595)) ;local v96={};local v97={};for v107=0,v95 do if (v107>=v89) then v93[v107-v89 ]=v94[v107 + 1 ];else v97[v107]=v94[v107 + 1 ];end end local v98=(v95-v89) + (1638 -(1523 + 114)) ;local v99;local v100;while true do v99=v87[v91];v100=v99[1];if (v100<=(31 + 3)) then if (v100<=16) then if (v100<=7) then if (v100<=3) then if (v100<=1) then if (v100>(0 -0)) then local v134=v99[2];local v135=v97[v134];local v136=v97[v134 + 2 ];if (v136>0) then if (v135>v97[v134 + 1 ]) then v91=v99[3];else v97[v134 + 3 ]=v135;end elseif (v135<v97[v134 + 1 ]) then v91=v99[3];else v97[v134 + 3 ]=v135;end else local v137=0;local v138;local v139;local v140;while true do if (v137==0) then v138=v99[2];v139=v97[v138 + 2 ];v137=1;end if (v137==1) then v140=v97[v138] + v139 ;v97[v138]=v140;v137=2;end if (v137==2) then if (v139>0) then if (v140<=v97[v138 + (4 -3) ]) then v91=v99[3];v97[v138 + 3 ]=v140;end elseif (v140>=v97[v138 + 1 ]) then local v355=0;while true do if (v355==0) then v91=v99[3];v97[v138 + 2 + 1 ]=v140;break;end end end break;end end end elseif (v100==2) then local v141=0;local v142;local v143;local v144;local v145;while true do if (v141==0) then v142=v99[1067 -(68 + 997) ];v143,v144=v90(v97[v142](v21(v97,v142 + 1 ,v92)));v141=1;end if (v141==2) then for v317=v142,v92 do v145=v145 + 1 ;v97[v317]=v143[v145];end break;end if (v141==1) then v92=(v144 + v142) -(3 -2) ;v145=0;v141=2;end end else do return;end end elseif (v100<=5) then if (v100>4) then v97[v99[2]]=v97[v99[10 -7 ]]%v97[v99[4]] ;else local v147=0;local v148;local v149;local v150;while true do if (v147==0) then v148=v99[2];v149=v97[v148];v147=1;end if (v147==1) then v150=v97[v148 + (1272 -(226 + 1044)) ];if (v150>0) then if (v149>v97[v148 + 1 ]) then v91=v99[12 -9 ];else v97[v148 + 3 ]=v149;end elseif (v149<v97[v148 + (860 -(814 + 45)) ]) then v91=v99[7 -4 ];else v97[v148 + 3 ]=v149;end break;end end end elseif (v100==(1 + 5)) then local v151=v99[2];v97[v151]=v97[v151](v21(v97,v151 + (118 -(32 + 85)) ,v92));else local v153=v99[2];local v154=v97[v153];for v249=v153 + 1 + 0 ,v92 do v15(v154,v97[v249]);end end elseif (v100<=11) then if (v100<=(4 + 5)) then if (v100>8) then v97[v99[2]]=v97[v99[3]]%v97[v99[4]] ;else local v156=0;local v157;while true do if (v156==0) then v157=v99[2];do return v97[v157](v21(v97,v157 + (886 -(261 + 624)) ,v99[3]));end break;end end end elseif (v100>10) then v97[v99[2]][v97[v99[3]]]=v97[v99[1 + 3 ]];else local v160=0;local v161;while true do if (0==v160) then v161=v99[2];do return v21(v97,v161,v92);end break;end end end elseif (v100<=13) then if (v100>12) then local v162=0;local v163;local v164;while true do if (v162==1) then for v320=v163 + 1 ,v92 do v15(v164,v97[v320]);end break;end if (v162==0) then v163=v99[2];v164=v97[v163];v162=1;end end else do return;end end elseif (v100<=14) then local v165=0;local v166;local v167;local v168;local v169;while true do if (v165==1) then v92=(v168 + v166) -1 ;v169=0;v165=2;end if (v165==0) then v166=v99[3 -1 ];v167,v168=v90(v97[v166](v97[v166 + (1081 -(1020 + 60)) ]));v165=1;end if (v165==2) then for v321=v166,v92 do local v322=0;while true do if (0==v322) then v169=v169 + (1424 -(630 + 793)) ;v97[v321]=v167[v169];break;end end end break;end end elseif (v100>15) then local v256=0;local v257;while true do if (v256==0) then v257=v99[6 -4 ];do return v97[v257](v21(v97,v257 + 1 ,v99[3]));end break;end end else local v258=v88[v99[3]];local v259;local v260={};v259=v18({},{[v7("\184\203\120\251\219\130\236","\191\231\148\17\149")]=function(v288,v289) local v290=v260[v289];return v290[1][v290[2]];end,[v7("\18\215\241\133\176\206\245\33\40\240","\69\77\136\159\224\199\167\155")]=function(v291,v292,v293) local v294=v260[v292];v294[1][v294[2]]=v293;end});for v296=1,v99[4] do v91=v91 + 1 ;local v297=v87[v91];if (v297[1]==(321 -253)) then v260[v296-(958 -(892 + 65)) ]={v97,v297[7 -4 ]};else v260[v296-1 ]={v72,v297[4 -1 ]};end v96[ #v96 + 1 ]=v260;end v97[v99[2]]=v40(v258,v259,v73);end elseif (v100<=25) then if (v100<=20) then if (v100<=18) then if (v100>(367 -(87 + 263))) then local v170=0;local v171;while true do if (0==v170) then v171=v99[2];v97[v171](v21(v97,v171 + 1 ,v92));break;end end else local v172=0;local v173;local v174;local v175;local v176;while true do if (v172==2) then for v323=v173,v92 do local v324=0;while true do if (v324==0) then v176=v176 + 1 ;v97[v323]=v174[v176];break;end end end break;end if (v172==1) then v92=(v175 + v173) -(1748 -(760 + 987)) ;v176=0;v172=2;end if (v172==0) then v173=v99[2];v174,v175=v90(v97[v173](v21(v97,v173 + 1 ,v92)));v172=1;end end end elseif (v100>(1932 -(1789 + 124))) then local v177=0;local v178;local v179;local v180;local v181;while true do if (v177==1) then v92=(v180 + v178) -1 ;v181=0;v177=2;end if (v177==2) then for v325=v178,v92 do local v326=0;while true do if (0==v326) then v181=v181 + 1 ;v97[v325]=v179[v181];break;end end end break;end if (v177==0) then v178=v99[2];v179,v180=v90(v97[v178](v21(v97,v178 + 1 ,v99[3])));v177=1;end end else v97[v99[2]]={};end elseif (v100<=(202 -(67 + 113))) then if (v100==21) then for v250=v99[2 + 0 ],v99[2 + 1 ] do v97[v250]=nil;end else v97[v99[2]]=v97[v99[3]];end elseif (v100<=23) then v97[v99[2]]=v97[v99[7 -4 ]] + v99[9 -5 ] ;elseif (v100>24) then v97[v99[2]]=v97[v99[3]]%v99[4] ;else local v263=0;local v264;while true do if (v263==0) then v264=v99[2];v97[v264]=v97[v264](v21(v97,v264 + 1 ,v92));break;end end end elseif (v100<=29) then if (v100<=27) then if (v100==26) then local v186=0;local v187;while true do if (v186==0) then v187=v99[2];v97[v187]=v97[v187](v21(v97,v187 + 1 ,v99[3]));break;end end else local v188=v99[2 + 0 ];v97[v188](v21(v97,v188 + 1 ,v92));end elseif (v100>(1 + 27)) then v97[v99[2]]=v73[v99[3]];else local v191=v99[2];local v192=v97[v99[11 -8 ]];v97[v191 + 1 ]=v192;v97[v191]=v192[v99[4]];end elseif (v100<=31) then if (v100>30) then v97[v99[2]]= #v97[v99[955 -(802 + 150) ]];else v97[v99[2]]=v97[v99[3]] + v99[4] ;end elseif (v100<=(26 + 6)) then v97[v99[2]]=v73[v99[3]];elseif (v100>33) then local v265=v99[2];v97[v265]=v97[v265]();else v97[v99[1057 -(87 + 968) ]]();end elseif (v100<=51) then if (v100<=42) then if (v100<=(167 -129)) then if (v100<=36) then if (v100>35) then v97[v99[2]]=v99[3];else v97[v99[2]][v97[v99[3]]]=v97[v99[4]];end elseif (v100>37) then local v204=v99[2];local v205=v97[v204 + 2 + 0 ];local v206=v97[v204] + v205 ;v97[v204]=v206;if (v205>0) then if (v206<=v97[v204 + 1 ]) then local v327=0;while true do if (v327==0) then v91=v99[7 -4 ];v97[v204 + 3 ]=v206;break;end end end elseif (v206>=v97[v204 + 1 ]) then v91=v99[3];v97[v204 + 3 ]=v206;end else local v208=v99[2];local v209=v97[v99[3]];v97[v208 + 1 ]=v209;v97[v208]=v209[v99[8 -4 ]];end elseif (v100<=40) then if (v100>39) then local v213=0;local v214;while true do if (v213==0) then v214=v99[2];v97[v214]=v97[v214]();break;end end elseif (v97[v99[2]]==v99[4]) then v91=v91 + 1 ;else v91=v99[3];end elseif (v100>41) then v97[v99[3 -1 ]]=v72[v99[3]];else local v217=0;local v218;while true do if (0==v217) then v218=v99[2 + 0 ];do return v21(v97,v218,v92);end break;end end end elseif (v100<=46) then if (v100<=(1457 -(447 + 966))) then if (v100>43) then for v252=v99[2],v99[8 -5 ] do v97[v252]=nil;end else v97[v99[2]]={};end elseif (v100>(1042 -(915 + 82))) then v97[v99[5 -3 ]]=v72[v99[1820 -(1703 + 114) ]];else v97[v99[2]]=v97[v99[2 + 1 ]]%v99[4] ;end elseif (v100<=48) then if (v100==47) then v97[v99[2]]();else v91=v99[3];end elseif (v100<=49) then v91=v99[3 -0 ];elseif (v100>50) then do return v97[v99[2]]();end else v97[v99[2]]=v99[1190 -(1069 + 118) ];end elseif (v100<=60) then if (v100<=55) then if (v100<=(754 -(376 + 325))) then if (v100==52) then local v225=v99[2];v97[v225](v97[v225 + 1 ]);else local v226=0;local v227;while true do if (0==v226) then v227=v99[2];v97[v227]=v97[v227](v21(v97,v227 + (1 -0) ,v99[3]));break;end end end elseif (v100>54) then local v228=0;local v229;while true do if (v228==0) then v229=v99[2];v97[v229](v97[v229 + (2 -1) ]);break;end end elseif (v97[v99[2]]==v99[4]) then v91=v91 + 1 ;else v91=v99[3];end elseif (v100<=57) then if (v100>56) then v97[v99[2]]= #v97[v99[3]];elseif v97[v99[2]] then v91=v91 + (2 -1) ;else v91=v99[1 + 2 ];end elseif (v100<=(127 -69)) then if  not v97[v99[2]] then v91=v91 + (1 -0) ;else v91=v99[3];end elseif (v100==59) then v97[v99[2]]=v99[3] + v97[v99[4]] ;elseif  not v97[v99[2]] then v91=v91 + 1 ;else v91=v99[3];end elseif (v100<=64) then if (v100<=62) then if (v100==61) then v97[v99[2]]=v97[v99[1 + 2 ]][v99[4]];else local v233=0;local v234;local v235;local v236;while true do if (v233==2) then for v331=1,v99[4] do local v332=0;local v333;while true do if (v332==1) then if (v333[1]==68) then v236[v331-1 ]={v97,v333[3]};else v236[v331-1 ]={v72,v333[3]};end v96[ #v96 + 1 ]=v236;break;end if (v332==0) then v91=v91 + 1 ;v333=v87[v91];v332=1;end end end v97[v99[3 -1 ]]=v40(v234,v235,v73);break;end if (0==v233) then v234=v88[v99[3]];v235=nil;v233=1;end if (v233==1) then v236={};v235=v18({},{[v7("\237\200\250\124\214\242\235","\18\178\151\147")]=function(v334,v335) local v336=0;local v337;while true do if (v336==0) then v337=v236[v335];return v337[1][v337[2]];end end end,[v7("\69\179\243\73\211\115\130\249\73\220","\164\26\236\157\44")]=function(v338,v339,v340) local v341=0;local v342;while true do if (v341==0) then v342=v236[v339];v342[15 -(9 + 5) ][v342[2]]=v340;break;end end end});v233=2;end end end elseif (v100>(1328 -(243 + 1022))) then v97[v99[2]]=v99[11 -8 ] + v97[v99[4]] ;else do return v97[v99[2]]();end end elseif (v100<=66) then if (v100>65) then local v238=v99[2 + 0 ];local v239,v240=v90(v97[v238](v21(v97,v238 + (792 -(368 + 423)) ,v99[3])));v92=(v240 + v238) -1 ;local v241=0;for v254=v238,v92 do local v255=0;while true do if (v255==0) then v241=v241 + 1 ;v97[v254]=v239[v241];break;end end end else local v242=0;local v243;local v244;local v245;local v246;while true do if (v242==2) then for v345=v243,v92 do local v346=0;while true do if (v346==0) then v246=v246 + 1 + 0 ;v97[v345]=v244[v246];break;end end end break;end if (v242==1) then v92=(v245 + v243) -1 ;v246=0;v242=2;end if (v242==0) then v243=v99[2];v244,v245=v90(v97[v243](v97[v243 + 1 ]));v242=1;end end end elseif (v100<=67) then v97[v99[2]]=v97[v99[3]][v99[4]];elseif (v100>68) then if v97[v99[2]] then v91=v91 + 1 ;else v91=v99[3];end else v97[v99[2]]=v97[v99[3]];end v91=v91 + 1 ;end end;end return v40(v39(),{},v28)(...);end return v23("LOL!0D3O0003063O00737472696E6703043O006368617203043O00627974652O033O0073756203053O0062697433322O033O0062697403043O0062786F7203053O007461626C6503063O00636F6E63617403063O00696E7365727403053O006D6174636803083O00746F6E756D62657203053O007063612O6C00243O0012203O00013O00203D5O0002001220000100013O00203D000100010003001220000200013O00203D000200020004001220000300053O00063A0003000A000100010004303O000A0001001220000300063O00203D000400030007001220000500083O00203D000500050009001220000600083O00203D00060006000A00063E00073O000100062O00443O00064O00448O00443O00044O00443O00014O00443O00024O00443O00053O001220000800013O00203D00080008000B0012200009000C3O001220000A000D3O00063E000B0001000100052O00443O00074O00443O00094O00443O00084O00443O000A4O00443O000B4O0016000C000B4O0033000C00014O0029000C6O00033O00013O00023O00023O00026O00F03F026O00704002264O001300025O001232000300014O001F00045O001232000500013O0004010003002100012O002A00076O0016000800024O002A000900014O002A000A00024O002A000B00034O002A000C00044O0016000D6O0016000E00063O00201E000F000600012O0014000C000F4O0006000B3O00022O002A000C00034O002A000D00044O0016000E00014O001F000F00014O0009000F0006000F00103B000F0001000F2O001F001000014O000900100006001000103B00100001001000201E0010001000012O0014000D00104O0002000C6O0006000A3O0002002019000A000A00022O00410009000A4O001200073O00010004260003000500012O002A000300054O0016000400024O0010000300044O002900036O00033O00017O00043O00027O004003053O003A25642B3A2O033O0025642B026O00F03F001C3O00063E5O000100012O002E8O002A000100014O002A000200024O002A000300024O001300046O002A000500034O001600066O0015000700074O0014000500074O000D00043O000100203D000400040001001232000500024O001A000300050002001232000400034O0014000200044O000600013O000200262700010018000100040004303O001800012O001600016O001300026O0010000100024O002900015O0004303O001B00012O002A000100044O0033000100014O002900016O00033O00013O00013O00243O00030A3O006C6F6164737472696E6703043O0067616D6503073O00482O7470476574035D3O00CBCF31F6A88B8C9437E7AC9FC4D231EEAED3D6C820F4B8DECDCF20E8AF9FC0D428A996D0E4D21DFE88D2D1D235F2BEC393942EE3A2C2DAC831E3B6C791DA35EFF4DCC2C831E3A99ED6D26AFEA9D4D1E428F5AFC4C7D22AB2EE9FCFCE2403063O00B1A3BB4586DB2O033O004E6577030F3O00DD33DD26CCD03EE82AC224EBD232F903073O005F9C43AD4AA5B303063O009A48043CA24B03043O0054D7297603044O00FF5D1303083O00464E9E30764272B603073O0009112450889A9803073O00CB44705613C5DE03043O00F438FA4F03073O0026BD569C20188503023O00F45203043O00269C37C7030D3O008C746F2B1C66FE6AA66B753C1603083O0023C81D1C4873149A030A3O0020ABFC8C9F7F660BB7F003073O005479DFB1BFED4C03043O007461736B03043O007761697403083O0046696E697368656403063O00436C6F7365640100028O0003443O00B342DDB0290A7F8EA957DEEE3D5924C9AE54DCB33F4233CEB542CCAE2E1E33CEB619ECA43D5519F8F45FC7A6335E39D5BE4FC0A536547FCCBA45DDA5281F23CEAE44CAA503083O00A1DB36A9C05A305003443O00415614355A184F6A5B43176B4E4B142D5C4015364C50032A4756052B5D0C032A440D29264C6F012045154F0B4C5529264C6A1527064F012C470D2237464D0B2D4854052B03043O004529226003053O007072696E7403163O008CCFD6130739FCC0DB05112EB883C302076B9BF6FE4403063O004BDCA3B76A62026O00F03F01673O0006383O006500013O0004303O00650001001220000100013O001220000200023O00201C0002000200032O002A00045O001232000500043O001232000600054O0014000400064O000200026O000600013O00022O002200010001000200203D0002000100062O001300033O00042O002A00045O001232000500073O001232000600084O001A0004000600022O002A00055O001232000600093O0012320007000A4O001A0005000700022O000B0003000400052O002A00045O0012320005000B3O0012320006000C4O001A0004000600022O002A00055O0012320006000D3O0012320007000E4O001A0005000700022O000B0003000400052O002A00045O0012320005000F3O001232000600104O001A0004000600022O002A00055O001232000600113O001232000700124O001A0005000700022O000B0003000400052O002A00045O001232000500133O001232000600144O001A0004000600022O002A00055O001232000600153O001232000700164O001A0005000700022O000B0003000400052O0034000200020001001220000200173O00203D0002000200182O002F00020001000100203D0002000100192O002200020001000200063A0002003D000100010004303O003D000100203D00020001001A0006380002003300013O0004303O0033000100203D0002000100192O00220002000100020006380002005E00013O0004303O005E000100203D00020001001A0026270002005E0001001B0004303O005E00010012320002001C3O002627000200450001001C0004303O00450001001220000300013O001220000400023O00201C0004000400032O002A00065O0012320007001D3O0012320008001E4O0014000600084O000200046O000600033O00022O002F000300010001001220000300013O001220000400023O00201C0004000400032O002A00065O0012320007001F3O001232000800204O0014000600084O000200046O000600033O00022O002F0003000100010004303O006600010004303O004500010004303O00660001001220000200214O002A00035O001232000400223O001232000500234O0014000300054O001200023O00010004303O0066000100203D00013O00242O00033O00017O00",v17(),...);
