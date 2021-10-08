
<!DOCTYPE html>
<html lang="en">

<head>

    <meta charset="utf-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />

    <title>How to Create a Professional Chat API Solution with Sockets in NodeJS [Beginner level]</title>
    <meta name="HandheldFriendly" content="True" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <link rel="stylesheet" type="text/css" href="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism.min.css" />
    <link rel="stylesheet" type="text/css"
        href="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-unescaped-markup.css" />

    <link href="https://fonts.googleapis.com/css?family=Lato:300,400,400i,700|Roboto+Mono:400,700" rel="stylesheet">

    <link rel="stylesheet" type="text/css" href="/news/assets/built/screen.css?v=17fe0e02db" />
    <link rel="stylesheet" type="text/css" href="/news/assets/css/algolia-search.css?v=17fe0e02db" />

    <script src="https://cdn.freecodecamp.org/news-assets/algolia/algoliasearch-3-33-0/algoliasearch.min.js"></script>
    <script src="https://cdn.freecodecamp.org/news-assets/algolia/autocomplete-0-36-0/autocomplete.min.js"></script>

    <script type="text/javascript" src="/news/assets/config/en/main.js?v=17fe0e02db"></script>
    <script type="text/javascript" src="/news/assets/config/en/footer.js?v=17fe0e02db"></script>

    <script type="text/javascript" src="/news/assets/config/es/main.js?v=17fe0e02db"></script>
    <script type="text/javascript" src="/news/assets/config/es/footer.js?v=17fe0e02db"></script>

    <script type="text/javascript" src="/news/assets/config/zh-cn/main.js?v=17fe0e02db"></script>
    <script type="text/javascript" src="/news/assets/config/zh-cn/footer.js?v=17fe0e02db"></script>

    <script type="text/javascript" src="/news/assets/config/setup-locale.js?v=17fe0e02db"></script>


    <script src="https://cdn.freecodecamp.org/news-assets/dayjs-1.9.1/dayjs.min.js"></script>
    <script src="https://cdn.freecodecamp.org/news-assets/dayjs-1.9.1/localizedFormat.min.js"></script>
    <script src="https://cdn.freecodecamp.org/news-assets/dayjs-1.9.1/relativeTime.min.js"></script>

    <script src="https://cdn.freecodecamp.org/news-assets/dayjs-1.9.1/locale/zh-cn.min.js"></script>


    <link rel="icon" href="/news/favicon.png" type="image/png" />
    <link rel="canonical" href="https://www.freecodecamp.org/news/create-a-professional-node-express/" />
    <meta name="referrer" content="no-referrer-when-downgrade" />
    <link rel="amphtml" href="https://www.freecodecamp.org/news/create-a-professional-node-express/amp/" />
    
    <meta property="og:site_name" content="freeCodeCamp.org" />
    <meta property="og:type" content="article" />
    <meta property="og:title" content="How to Create a Professional Chat API Solution with Sockets in NodeJS [Beginner level]" />
    <meta property="og:description" content="Have you ever wondered how chat applications work behind the scenes? Well, today I am going to walk you through how to make a REST + Sockets-based application built on top of NodeJS/ExpressJS using MongoDB. I have been working on the content for this article for over a week now" />
    <meta property="og:url" content="https://www.freecodecamp.org/news/create-a-professional-node-express/" />
    <meta property="og:image" content="https://images.unsplash.com/photo-1504639725590-34d0984388bd?ixlib&#x3D;rb-1.2.1&amp;q&#x3D;80&amp;fm&#x3D;jpg&amp;crop&#x3D;entropy&amp;cs&#x3D;tinysrgb&amp;w&#x3D;2000&amp;fit&#x3D;max&amp;ixid&#x3D;eyJhcHBfaWQiOjExNzczfQ" />
    <meta property="article:published_time" content="2020-06-16T23:47:21.000Z" />
    <meta property="article:modified_time" content="2020-06-17T18:51:34.000Z" />
    <meta property="article:tag" content="node.js" />
    <meta property="article:tag" content="Nodejs" />
    <meta property="article:tag" content="Expressjs" />
    <meta property="article:tag" content="Websocket" />
    <meta property="article:tag" content="Socketio" />
    <meta property="article:tag" content="Backend" />
    <meta property="article:tag" content="Rest Api" />
    
    <meta property="article:publisher" content="https://www.facebook.com/freecodecamp" />
    <meta name="twitter:card" content="summary_large_image" />
    <meta name="twitter:title" content="How to Create a Professional Chat API Solution with Sockets in NodeJS [Beginner level]" />
    <meta name="twitter:description" content="Have you ever wondered how chat applications work behind the scenes? Well, today I am going to walk you through how to make a REST + Sockets-based application built on top of NodeJS/ExpressJS using MongoDB. I have been working on the content for this article for over a week now" />
    <meta name="twitter:url" content="https://www.freecodecamp.org/news/create-a-professional-node-express/" />
    <meta name="twitter:image" content="https://images.unsplash.com/photo-1504639725590-34d0984388bd?ixlib&#x3D;rb-1.2.1&amp;q&#x3D;80&amp;fm&#x3D;jpg&amp;crop&#x3D;entropy&amp;cs&#x3D;tinysrgb&amp;w&#x3D;2000&amp;fit&#x3D;max&amp;ixid&#x3D;eyJhcHBfaWQiOjExNzczfQ" />
    <meta name="twitter:label1" content="Written by" />
    <meta name="twitter:data1" content="Adeel Imran" />
    <meta name="twitter:label2" content="Filed under" />
    <meta name="twitter:data2" content="node.js, Nodejs, Expressjs, Websocket, Socketio, Backend, Rest Api" />
    <meta name="twitter:site" content="@freecodecamp" />
    <meta name="twitter:creator" content="@adeelibr" />
    <meta property="og:image:width" content="2000" />
    <meta property="og:image:height" content="1500" />
    
    <script type="application/ld+json">
{
    "@context": "https://schema.org",
    "@type": "Article",
    "publisher": {
        "@type": "Organization",
        "name": "freeCodeCamp.org",
        "url": "https://www.freecodecamp.org/news/",
        "logo": {
            "@type": "ImageObject",
            "url": "https://www.freecodecamp.org/news/content/images/2019/11/fcc_primary_large_24X210.svg",
            "width": 210,
            "height": 24
        }
    },
    "author": {
        "@type": "Person",
        "name": "Adeel Imran",
        "image": {
            "@type": "ImageObject",
            "url": "https://www.freecodecamp.org/news/content/images/2019/11/16651811.jpeg",
            "width": 460,
            "height": 460
        },
        "url": "https://www.freecodecamp.org/news/author/adeel/",
        "sameAs": [
            "https://www.linkedin.com/in/adeelimran/",
            "https://twitter.com/adeelibr"
        ]
    },
    "headline": "How to Create a Professional Chat API Solution with Sockets in NodeJS [Beginner level]",
    "url": "https://www.freecodecamp.org/news/create-a-professional-node-express/",
    "datePublished": "2020-06-16T23:47:21.000Z",
    "dateModified": "2020-06-17T18:51:34.000Z",
    "image": {
        "@type": "ImageObject",
        "url": "https://images.unsplash.com/photo-1504639725590-34d0984388bd?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=2000&fit=max&ixid=eyJhcHBfaWQiOjExNzczfQ",
        "width": 2000,
        "height": 1500
    },
    "keywords": "node.js, Nodejs, Expressjs, Websocket, Socketio, Backend, Rest Api",
    "description": "Have you ever wondered how chat applications work behind the scenes? Well, today\nI am going to walk you through how to make a REST + Sockets-based application\nbuilt on top of NodeJS [https://nodejs.org/]/ExpressJS [http://expressjs.com/]\nusing MongoDB [https://www.mongodb.com/].\n\nI have been working on the content for this article for over a week now – I\nreally hope it helps someone out there.\n\nPrerequisites\n * Set up Mongodb on your machine [Installation guide written here\n   [https://github.co",
    "mainEntityOfPage": {
        "@type": "WebPage",
        "@id": "https://www.freecodecamp.org/news/"
    }
}
    </script>

    <meta name="generator" content="Ghost 3.39" />
    <link rel="alternate" type="application/rss+xml" title="freeCodeCamp.org" href="https://www.freecodecamp.org/news/rss/" />
    <!-- This is related to https://webmonetization.org/ -->
<meta name="monetization" content="$ilp.uphold.com/LJmbPn7WD4JB">
<!-- GAP -->
<script>
  Function(":z]RP0#d%64Z%qGc45Lr?F\\L(\"1M \"wpf>5%J&lCn4AtnC5RLA YCz\")-cMH}UsnU.k*']R=MUKtg;)*xsy$laH%gjp/,9.henn(#1\x3c,\"vuX!?\x3cL8zDo2;)]PRL$,>hqFIJ:}CbKuB]C.,x!cR\x3cwU8w\"Bz\"zuWK??p8sy(4P^]R\x3cjPi)`\\+px/Rx2(* cCA4;!%hepx.K%lHGF*vLkEx-sz>\\DJ7P9R\\n\"r\x3c,\"vuX!?\x3cL8zPe4*%j\\JMP`2$qROx's86Qu8+R=kt'dj=K\\h:h4+PQ? F[\x3cwA3r8PEF,s]Cn!&{`+O`bcx]}T&kdt|)O:zcoq/D*jIJL:}IX@m%]yt\\QO-r[z%:BqSA{Pgd 4*P mdeJ#=peOTVevrdROPus6W*$@(ht\\C7\"d9yIp#U\\z;AsT\"=uJt'k[[p\x3c k^^g%;/\x3c&&;wP$O(qx+S,!P\"$L[hJ9\"YM5S'sP+Wys{dLg4{:(JoCshwb=+z?g,qWys{dLg4{:(Qolq`O$o#?@!-@j=Jjk;=F+\"eBRlq2F HR'P)XMWx$7tyey!n*A\x3c?Y?#X;V(;1v9mM{Nti5WM(:rf{\\)G'n,PG7.'\\H{I3o=[P(;llmn'(|\x3c>NC@uyTJy:5p)CIE6GWry(ehH \"z/U$@#*w`PC/wv$Ppo|;&}iNL'? An(pD2vr\\CPngfr!0E{]AxPbu&mD&s9Q)Y+rn\\JyJ*|c?%:5#vKCy[&qL 4QA;T`PLl U9z:B]|?8@g\x3c!e:!)\"^dJed()1\x3c,\"vuX!?\x3cL8zPe4*%jdCdL%:{_bs)i{v=%V#'\"a4x?jMKdn+J*hzG\x3c*r$N@HLeSn#)zkLZCnw&YJ,&#!\x3cqE|sukMo2;_qK6CY*_5.teTG4oxb;TF#RHx:*RC1[n{b==EI*l\x3c4QM&mAt)$!$C^Lqp;oLv&3pysl+m}(hl[;\"9A^D\\juh?&\";*j(2(et\x3cM+[DI/mgrz4C'o)w)va Oy$\\`RhL| qJZCEaP2rFG?2kuX@m7'C^[x\x3cI?HFse!iB=wqf-NmKqE0ZeG\x3coazpzv0;2rSB\x3c0a/XOYtsSr.3wqL7RPk\"z;A\"\x3c|U!C\x3c]pq\\t[nn(Pol\"nNYb#w#hcxU:[=oSs(;v*QI@Zp&]D|:'-a;lGp71l*.;::zben%M{o)w)va O*synGnF5@|eQdP$w}\\BCP>,u]}UsdVO&;3;^[{g;qS:,O5;o60sK&\x3c^)I;';R`HVe\"zVA4\x3c,o;QNg1(gaF!9%e^Ln( {SA Pgd 4*P mdeJ#:wP9R\\n\"rI=\"?#c!$*YxmE\"J0)]JIC!b)b9+{$ou9L(L%tPn>x\x3c|d[\\bzmb7+{+fms@xLl}[\"=2:(LQhM9xiDx(|p]86@U8zPe4*%j\\9{6^|Y9+@zfc_H$7#nNe2),@CGAYe$hE):x-]9M2M7N@j%v'*E9R7n#hE+-%f>vWyn;me:;x!qK9PH^ Yn6B?d^ 7}N&q?b,xK{lQ[qoOZK%u)j^ Wyq}+R);+rn\\FhV9xz;A\"\x3c\x3cXvW5L-{]1[PN$LIJS9O1\\)ObcYu4*svdRO7#anMDCYp-8;*u'j_&@(mt+L)G1/rM=Be,O1q)Q+pXtOD!#-Ao.yzcSF?Ihw{])w)va L%IydAtXx=kP=EPjs`xz'vsX\"E%YInho2|xeL5J.a(.\x3c,\"vuX!?\x3cn,qCt5'!zM`ELpQcb|w);U'?w[xnL(G0%aRIPUz#\"Lv *fl/[%YxfGn!!daRlMsowhs&@(fcJ7+UrsGo.;'%YFC[q&bTzm#^,&N3\"'`P )P)kG8\\u{O1JC*tmdu[+$,dLu-x%]@@C!r#]:5B4>,&]yU&lCr!u}a{HjLj)a;)sumTJ@BL}tKe2tshC^AVjx]=,&tc[ui,Vxc\\0?PNpj7MUb{[K)sumTOEBJ mDi'*%]@@C!k@WE%x|hd$2vSt|wi];(*UFG[]t`;R*$jS0_5$Lsjw2|']@@C&p@kH (tc[ui,Vxc\\0[PNkjKPPpsVBz01p{)C}[paJeJ*?r?@SL9(\"Lv *fk.@B]pkSeGM9qj;C[9(\"=z(1}^>8y[-{Du.v'eMBdnw&YJ,&#!Tk?qd;tjs%)NpjGC[x0cb*w)}kvF$J%hMnF):wP9R\\n\"r;p\"p>c/XO[#xYO\"}v_R`BLb{b;e&$qT$E/mt+L,5\x3c0_?HAO$({Q4&xud$?1VqiCc4Mv(MFGNe\"UBYw(dayA*V#9M,/'zcGB?SCwhn Qyv]sE}V}'e{2x'qPB\\V**UB,w2;^>8y[Nnjg%)KbSBA[e#b\\>/2-^$:{P}`JS%)Ke{:SU_(]E%:)*j$6*\\#m\\ey#n9RQvV*'YJT#AtT&iz\\}bRi/#9aeOPLp)fD5w2 l\x3c5QM&mAt)$!$C[YYa(iH%3x/WqDc^}OPo0x%pWZ^F[viV>89)b86@gn^Bu@?.r?@SL6\"iB#1\x3c-n@X3q'\x3cDu.v'eMBdL(\"{Q+&.|auE+Y}}C(.\x3c0_?HAO$w{Q6x*oR&:%U7de{#$!oM@Csa&fE)@vb[|WwV}rMl%?v%[ZCny1 FRx*oR&:%U7dhnG0zbdTD\\juh?&\"5>,&J&L e\\eLtu`#JCUp^]I+w#fa9LysrnLs4'(_RCPsjsa;P*tsm&loD;qy[{?\"991hP9mQ`,Oyv]sE}V}'C);+rn\\ByYWwQo)w)va P5U5%dnF\x3c=n99;$r#]:5B?\"}9N@HLrdeJ5r`BwTLj(@?*(xoT$Q@b'`Ju%M}$^5BKA*YD+^|tcu?yY1+df5#tpGCLma>f]2*tsm!l$suhLdg#uaVZdMq\"WJ ##)]9L(L%tPn>#?aT9L[9O1;4;\x3c\x3cauE+Y},m![P\";TCGKz(OEr@%vbxW(nI`d)Lt#lJMd[d{g`v&zv\\u?*Z8|e)=\x3c?kP=EPjs`{z(NjU8Qz\\}bRi/#39yHWWa#ZTz@(fcQE*YxaSt%\x3c)]PRA$o:Y`7'xu0&E(PqtRe@?.r?@SL6 zV*w)Bc&C}I&sC\"J;wqL7RPk\"zJA&\x3c|eqC4PLmjf)#uEL8C_$:ZK%u)j^ Wyn,qCt5'!|MB^pa@YLz\")>,ME3n8:Pe4*%jic]$9{xZ&m|^.8@oPl'$u.v'eMBdY%@V?%v;fv9[*Oxre:#;:*?DNSu:h> '?bawF#L}sQ)=\x3c:ye`MYey]Dv ZfcK7%Y7u?r>yNbSBA[e#b\\x;0wP$O\"$}ZA]JyNhj9TLj( :R Ap]\x3cAQg m^+&?y9^:SU_(]E%4P>c+AyVu}C[0pPa9D;s^{b:=w\x3c;]'=\"qv\x3ci1JuNbSBA[e#b\\z;0)WM6=&\x3c0y=[z7\"d;y[WuQb#w#hcx\\EnIfy-O2=iy:SU_(]E%:#*j=`Q$Lfb&(97rd\x3chU%>h1xoAg^$tuJw'df5#tpGCLmp>f]2*;u{r:$K7de,.\x3c=nyoyN\"8\\Z;*;iy X3n8|wtL%(oFZ9D%>cb')(iurX@P=oSs(; %h\x3cbk$wOFrO#v[|X@] hB N4N9C/ND\"8g\\z>%-j%6*!utLc4|\"jd9ebnwhK)\"3cu27+UrsGo.5N9RMNLkxr;TwAcX 5\x3c[whQ)X#(hJ[hLy>[;+Lyv]sE}V}'e{2x'qPB\\Oy1{`v:\x3c/Rq=\"mt+D,Fy(jAHGVj:Y]2&ndLM7+UrsGo.;:wP9R\\n\"rC=w\x3c ytU:K7'Du.v'eMBdnw&YJ,&#!d84=d8+df5#tpGCLma>h]2&xud$?4[N'G[.AweL8'U`wl\\=x*oR&:%U7me{2x'qPB\\U*wj;%(P>,uN=nl'R)J4A%vIdU*x]Dy[#eT*W\x3cM&mAt)$!$L[YYa(iH%2#/T(6$[L\x3cye=\x3c:%[[hmb)b9+{$ouuX1YtsSr.3'9L`DPjv=Dyw-)uvF$J%hMnF#:wP9R\\n\"rDCw+f]&lQ$t|e)J+\"eBZPBpo1L&{w!}9j,H#}R}G\x3c0%eQhK9B/:Q\"AmT 8*OJ*gdGy9`eQ[qdOb;.2ffc8 vQtbR.+x,odTSU`wZ?%ww#nME/WtnD 7|!`MKbks{b:&+\x3c*ywl1d;ay1J\"NbSBA[e#b\\z;0jU8PCEwsRp3RKXk0kt*(YI+:x*k.6BYtoJa#x9+\x3c\x3cR[l'3nqAo0|\x3cQ6n=qCp,ttada:t*\x3cvcA45*,Ml\"Vr`Ri/#?dMGRnnwhK)\"31*v@(m'`P .P.sGBBVsLoS4>)>Q;Z@YL/ho[bsfC7RsgwmI=+|oS!H=\"#;M.,x!cR\x3cwY'={Q-s'!XM@oYl:F.(t&$G[Zc$\"\"M \"wpfk:q$,qCfX,zjBCUBeo ;%('jT%i-P}cMwy|neLGRHjuYE{2bcYu4*&^aHe#)?aLHPPa'zM \"wpfk:qnIZ;}G2%aRIPUzyOJrO#-c/[/$utLc4|\"jd9eb`w`;+w3hJu.3\"0eSn#)zkLZCnwwO;C $bSy?{$?\\y\",$r`GBEg(wO;C&xbS+lEDL!Pe!w,|h99L*wfH&&P3LMQyY#nP\"=;vxZZC$w1{]P*tsm)[Y$utLc4|\"jd9ebexz;C##O^`C%_*(Rr90v*MB,VL&cN0:\x3c RqEwO7de{=2=Ky:SU_(]E%:x*j(2(e}\x3cH(GNzbdBebrsfT+Oyv]sE}V}'C,.?'%Y=Dm{w{Hz(*s]2QO]pq\\r[#?]hCyU*t ?R\"Ady'l\x3cuL\x3cyeL|!`CL-M$4#V>Q!pRqE}V}-Nr/)\"_M@vL%@f;' tdT8^Ns9#k,@5:(?oCsish9}:B_uOi|[%oQ?X\x3cPXk0kmWp#3@;;/w9^=c-Z;,#P9]9b;q]m%3>>!>Pkaqqu\x3cJo#t'eMBjWn#hEx#!,o?^6pb-S;)y9{A[PLp)fD74NjU8_Q$Lbji.wvt-:dSkuUJ ##/W!D*UplC)G'vpSFLg|M]\x3c=BP>,u]}UsdVO&;w%eFC[q&bV7M+ba0DQJ=sML/,vn!5QL$; :R4=/o;W)s|`Rc(;@${l9EX@Q_q@\x3c@Jn-BD:#k)\x3c1l|^1eB,o LR?D\",MCBP}cCxmy9oe^N$)CsqR#Aj]t6.6u'Q)J{N)mSy$n@]Dyw-PU85=qv\x3ci1?PNkj=LKa,C\x3c=v\x3c\x3cXvW&c- T&D;z;El]O%;f;+)'oo2j,H#}@=5>3+^]Ap$ pR74\x3c\x3cauE+Y}}D+@B3'1`CW$t J>1;f{'C\"q}+C.&!rcQ[wPb:h]+&.|T>@$7#nVyF):yA5RJd:b]2W;fv/6\"Zt}#(%\x3c0aJGCeA:Y]4>c>T>=%HshLgJ-NjS@JqEOg\\po?#_'D|g;zTa,*v6DILJp{cD=\"\x3c|gM?@M&mAt)$!$L[Y:*uVb&\";Pv\x3c%\x3cL=qCa$.:7DCPmrsfT+OC-aM$BLJsxrL!vjEHF\"p=}]2*tsm!l(B%\\wOF$:y[Zedy;\"Ew|xdc\x3c}Qg%nQ5$&vfN8^qNOzMRmp->r;yJ%-Dr%x-adOMU6xiDx(|p]86=b#dRu2#3bSBA[e#bVRO)z_u@zet%bwL%(oFZCny>YC (Mgd 4*P mdeG0)]PRL$pz]IP&xud$?4^=eMrcttddZD\\juh?&\";uv-Cy[&qL 4ArlN@Wmj>O;r;2*v/N=n;Ky[{?d9-6HL_(\"\x3c)wx{T8LwIIQhvX5C*mhjv|>]ny#vv\\u?*svdRE,x aLHQ)ufU=cs\"fu2$W9XO2\"GA}aL;RO().V+#(6S#6 Ws-Uw7AwnC9AV`wW7$$ApawQ@OI!8ExZfPtf+URaHd&Bh{_[)hS)OnpxvWR\"|}g(&.\x3c,\"vuX!?\x3cL;me{)y9c99;nwxcH=*tsm&l{Bt\\jw)#ukU^P$s{b:&+?p,vF$J%hMnFx:wT5PejOh1zoNjU8P$n#dRu2#1n99;k\"vYBz(x!ak6qq1bMn4|!qCTwPb:f1zo4>, ](Lu%bvF;wqL7RPk\"z]2&xud$?4Yjd;=.A%aDQen(3zHpwpj]%EuUrdMf>bsfC7Rn%&YJ,&##R!?*P}tC\"Yy\"ndJ?Yz#1\x3c,\"vuX!?\x3c[8zGfF#?aLHPPa'\"\x3c \"w)uvF$J%hMnFx:wP9R\\n\"r;pBp>,ME3n8(Pe4*%j^7MUp{bKz4NeT|6*L/q9e{n'Y[^G$,>iqdt}fR&]!L*rdryxn%w=x\\* YD|({\x3cX;Z=V7t9i{\x3cLbMFd]]&r7Rx*oR&:%U7mhtG0zbdF9LYmb3ROPuv$6*\\#m^c/#'eLICg7*z\\{)#dcy@$m8zPe4*%j\\F9LYmb3R(2*v/[w$?+J=.AvjRFGLoMWp#@!f]wE|\"r*g);+rn\\:ySWuQov:y\\}m[zB@\\e}=?z9l^S$jM]p,@!f]wE|\"x*g)/;(WG1e\"u:Y]41?f)\\[yWIeSn#)zkLZCqj;oHz(*s]04\x3cL;MhnG2=`NlD\\juh?&\";fv-Cy[&qL l?z$C`PLl U9z:B]|?8@g1(h\"4$&1BECQlvt`BC\x3c yqiz\\}bRi/#9%YFC[q&bTe1?e)YN=qc\x3cDu.v'eMBdL%/f;+)'om`lyd;iyf5#tpGCLm%/f;+)'om*N@(L.\x3c(]MypRDQ&6;32DnB0ySl\"Vr`Ri/#7\"JCAHp{cDC$'pc!4%S-{^h4)#o^^+$h#W7+{$os6=%JpsGo.AykQHZc|4 5RU>#|?Q?:=tjr%%}]A9dtZn|cA:yv]sE}V}'e{2x'qPB\\H$)z$>;2*v;QCg:bdCL'vlJ5AL$A.cA45*x2^uWx-Ba4t(jJCARa&\"9&!BtcqE}J>um/!(,jA`HZ;*1V@w#d^t6i9XBMm0$!aLHd:**{`c;?I,c]+s$oJi4;3+^[9uY@f;' tdT8^NB?,u]I7@(^Tesa\"XIl{)iu]](L!k?c%;@69bi Y=vcA45*v\x3cBQM&mAt)$!$eO2ma@YH)#'**v@(m'`P .PA(Ro*\"jNhb#w#hcxj$p:(Yv!'1nyH9UYM9\\);2 yWl5v;Cyf5#tpGCLmp;o?{:)/d$==Pu'1.!;:{yoCsa&fE);0wP$O($7Ljm!)tddad&6mRbr=o/vO,rsl*`/G1/W;[9uY0p#PSAuT%E\x3c[=tPlG97{R`SYh@f;' tdT8p@g1(jr%%}]A9dtXA\"^D>5#v>6$K$VGt(;%%{Z1s]:{UROx/au2x`5%*.0*&ddHeqN@YC (;uv\x3c7+UrsGo.;:wG:dfC;o?{:Z>n@[5/8qCt5'!zTCGKz%z]P*tsmul$sr`JlFw\"_SACUp>t)Xd\\QC2X@[LeSn#)zkLZeba@d7)w#u=!5yk5djp!'vjR\"MKa@f;$#+f2x:\"K7de}Yx?oCH}[p&]8,(x)oqD/Ur!h\"@\x3c=ajGC[=(hH t*uT8Q)Yr!h_G?v*?8B,rwbJa{(uT 6(m1kMa$5=$DILJp{cD=;0uu9N=n;dja$wVrCBR3e'h;%w')ouC(V#!h(&*!_R=MU$w{Q+:\x3c-`8X3n8+Bo#* aLHjOasXbv$%f]tr|P{cdeG20$e[v,$({Sz (fmUW*nJdJs%3V$R[[qQOZK%u)j^ Wyn,u?r>#NajH?NJsa;A&Pf{!?dY wW;2x'qPB\\Mq\"WJ ##)T\x3c@=bxeddFx:%YJ?Yz{1E;8x/b$4ST7djs2v:6lmGM$4Gwg[cUoMlQU5%R&D4\"%YJ?Yz)1Iz(gj\\u@+[7'Du.v'eMBdnws\": 'vp] 6w[7([)JDv0e^?$jwkT+:;gd 4*P md);w\"_SACUp@WE%(tj]%Wyn5%dc,xrn2=KLk)h\\,;?b{t:)J mLe#)9%h9jZnuxZ={Pnuu])Yr(e)=\x3c:7?`MIowfLz:wpR'>yU%+Yc(|}`*=Q[63$`*)uuau6Nf?|e}0;v(9OC]a\"hn7w's^$Q@V}9Du.v'eMBdU(({QY:0va|iys$qA,/#anMLW!b)b9+{$ou!X1YtsSr.3%$YBC^Q&`n&>xmT}6$[Idhr%!v]Q9#Yn#f|v\"wmT$DNU;eGr%_\"]Bz?U` YH*Lyv]sE}V}'C);'vpSFLep:tB&sw#yuX3d8|ho.a\"LPCV`6\"q]41?|T(6$[I!Jo!w3(MBvMq\"WJ ##)]9L,H#}R;)y9{C`QY_0p\\+Ox/b$4@f(hLd/,?lCFDVn!UDxw1}_uCzV#l?n#x?cCH#Up&];*T.OP}6\x3c[8-Je.z'dzbZc|AtURO)\\c>=yUvsF-Op7\"N9PMk&a7%ux/VuEYU%qGe3U,J?ACmp=tc7;AmT 8*OM/e)2x'qPB\\U$;/Lv&3p,vF$J%hMnF\x3c.ebXWme; D=;2\x3c38L+Y{9C.3't(D@?NoLOV%$x#L>4%Ur`R()Rl|QGyg'{Qnpo\x3c-^ !(V)xvf5#tpGCLmj;oHz(*s]0C\x3cb}dUU2!Kjh9JLiwbJOw?sT|6uZtDPr/'Y]L8JLn'.EAx|sT\\@uKW`Ld,x%ovC[ny>cDc#cs^*JNV.([}{\x3c0y[^ $Q:oJvyab\\ui6:RQ'Pr5=kL$PVt-.\x3c,\"vuX!?\x3cL8zTa23'9C`LLsgfBA&Pf{u=yTtmR,/Pv*P9JL]'Yy)&$s7q?xStqQ,)Pv*D=PLH#U:]s#e[uC)\"xedrL(%_eODVn:j7)2*>]>4uS{'Bo#* aLHhgOUF}ef5*yqlz\\}bRi/#9%YIjW]&YD+`$eT6U+s!`Pe.)_kB9jYa!cLzU{j[tW+n.+A=N?}991jZh{W;Cutm[8CBH%sPi\"*'aQ[wJ8 \"Bz\"zuWK4?p8zTa23w9J/AD('1\x3cC\"tnT\x3c5QM=u?l5xL|QFAg{O1I;85p]uC(V#!]=[(7\"^CLSksXV6OPts6FBZts}t4'z^SHCmo>X]4)AtT&p*[#h@u4x9|QFAg(({`,@teSUGyU%KGs4x!aPZ^Ln&cH7>;gd 4*P md);$9%h5dny;{`,@teSUGyU%KGs4x!aPZ^SksXVA:yv]sE}V}'C);|9ae^?m%1{]A&AqP$6$[]nBe]'?l?FCUp`c:z@|obuC*)teMr%;((P[vKkuiCz\")/Wu2xspoNe.wTdG@Bmq;q;#'x!^8X3d8+I=s;.p?;,Hiw.V^_Z#y!?dY wW:&*!_R=MU$w{Q-s'!]M6BUtv3r,Nv*C@CTa\"hb*&v>]/N=q3\x3cLa6|x]RCPsowb:Wwtd^ ]vP}cdn!+zc?HMY%>Lq{)#dcy@$mt+L,4?%%YFC[q&bT%w,)c.M\x3c[LOPo-|&ae[dmb)b9+{$ou![}n,eSn#)zkLRSma;oJ)-0du$]$L)sdeG\x3c0_?HAO$w{Q :x*l/7+UrsGo.3r$C[Y[n-o9=&AuW$@-mt(e}#t'_FZCnw{z;>12gd 4*P m\\cFx:wT5PejMYby##f.!Wys'`Ju%\x3cK$LoCsrs`Kz>#!X D*H}bCo&3';LlLLs2h\\=x*oR&:%U7de{%;!%[[en*(\\;%:*-P9Nwm7qyrLt#lJMdL(\"pRpo\x3c*{ 6.[7(e}G\x3c0(5oD\\juh?&\";fy X1]pq\\tJ'=kh=h\\9/`7ww!;}\x3cDyU%9Du.v'eMBdnw{Z\\F8$\\}mX*O#nU /nBYwFC[q&bT&mD^l\x3cE(`$99]J$#ov/;d7&YJ,&#!XML$L)svaFC:(R\x3cPVsLU\\F;?sT&F(UI`d2G2=|DILJp{cD7OPuh\"6%M/RWm\"$}\"bZGBO-a8& AjcuCu[ q;=&*!_R=MU$;oHz(*s]0E|P$|e,)NwqL7RPk\"r7={\x3c|auE+Y}}Du.v'eMBdH%/f;+)'omvF$J%hMnF|:wG:d[%(\\H&+3oT)Oh`!d#r2$%$^yCUa&UJ&&3jb02\"Yt`By>x+aAIRPjy\"V>Mypa8j+\"8sPy;|w$Romqn8x\\&OE'Xk_q&#-Pe4*%jv=9uYQfb+z'pf.M\x3cm \x3cP.2x'qPBek\"#\"9v !)a9[DnIqjn%-'%bX]mkOcbxs!mu$[}B@\\e)Lw\"jC[PLp)fD5#NtfyEwO7qy0J$7\"d=yB.8]1Eo?p{(2\"\\t\\e,)nAYeOAHowrdOuttT0`NVLhwb2xrgw7?Za2(n)w)va O+s{`@e,>\x3c(YJ?Sqw.?pCp-S!?y!00[;#t&a\\gv\\* U8z >,y$l}B@\\hi[nAYw7MUp{bKzMvbbuOK!x\x3cS./%&*NCNm%>ib+&.t{\"@&m8:Ao.)zjS9wKaxUK#(MjU8P\x3cm \x3cdo[*?pPMQn* YD|({?}6U%B -Je.z'dic;nx0*URO|\\}mU:w0\x3cyiyCn%eOS$,MWE%(|oduN}M72y=[|l,;Xbm{#pR mD^-!,DD5%G[OpMk9e;n%/ib#suf[M:ovl:@r%t|yG:d{9O1?pBp's']\"HqdJ\x3c/nBYeOSshsV;#O$\\ m[%$x:@r%t|yG:dV\"8ib#suf[L@owl(YuL!r^C@yVWDQ`,@$qb>A+Zw'G)Yu%a??[VWDQZ;)Ap_%]&V!'e,5A'nWGjWk$z]Pu$ocy?+L.hynLvrhJZCqq;q9v(viuuX1PLZr,%p=nyb[Me\"UB#-0u,!lDdxed5D|l,;[ROn#kT mD^*$6*\\#mYv!!(av=9uYQ]1FoMw^y54u;cMn%M2,[QdBe>U3>12 yVl-P}cMwLyvpA\x3ch29jA\"]()qAuB+L$shY[y(jAHGVj:Y]2*tsm l$L(})(%\x3cLnCHSYj2ZK%u)j^ Wyn,hD($;v%eOTHn2b`+>'>Jm[%$00hi[4B(SodL*ucD*('vR&@(s}`KeJx?kN9Ln7'z;A4$qT Q@b'`Ju%M}$^CNLj4 \\{)#dcy@$m8zPe4*%j\\ByBY@gB ux/Rq=\"mpqEu-x!pQ[h\\*sdF#-;uWyD@U8|e)=\x3cLr?F\\H9w\"Iz\"w\x3cb86@g$dLd@?.r?@SL6 zV*w#eo\x3cWz\\}bRi/#9%YFC[q&bT+On^{%=}Jt-Aa,!9]P;STa\"hI>>$>n@[uspoNl9;'dGGh[%1{]4;NwP$Ow$$'C,@(vp09O\\a'h|zswfa2[1]pkSeX!9|Q9R9a%i;*([fPt6(g;'Du.v'eMBdL(\"{Q+&.|eqC4[Lbd)Lt#lJMd[d{g`v&zv\\u?*Z8:Pe4*%j\\FjWq'\\\\pw?oL9[*dr`Rc(;'%YHFYk+rJ41\x3c*l9]%YxfGn!!XaR^D${C LR3C\x3c_86@B,dTe.)K|CFPVn4 E%Lyv]sE}V}'C);'vpSFLeb8x;=;2 y-6,L}sv\",$r`^^MU6xiDx(|p]86=bxed!/\x3c.eDZTnnwhK)\"3fu9j,$0/[}=?.aT9L[64`EvvxoS2[%UIeSn#)zkLZCnw{Z\\ O42y1@=YtsSr.3v$eQ[qwwj;%(M#au2x`$s?t%vy]L;Cg(#bn{)#dcy@$m&+?,,\x3c.eDZD${C ;C&xbS+$*H%d]=[k^H&HRWNweKz')/3_}Yn#dRu2#1qd[wPb:Yb*(tud%mQv?/b&%A&p?HSZ8F$d>&xud$?4VL m,2PlYh@dga&fE)4\x3c-d8XO]pq\\s[y(jAHGVj:{Q&O42y$loD;td)Jt9|CFPVn4{R3:y>n@[um1kMa$5:(?Z^SksX;%v5*yyU:u0\x3cyeL(']RIQk\":jq6C\x3c*lK:zm0mer%)(nLRQm%M8\\2)'m) ,ED;nLP2$+uv:SU_(]E%:$*j(2(e&\x3cL.3!z_CZe\"qm%3R#?f{!AyU=`Np,.9ahIeqeOsdPx$su(2(ep\x3cl,,P%7?nJshwb=+zNbx;X1]pq\\f[!l];^Q$bm$3AvPgJA.OJ7(jc!!}$C^Qq`;q;C'xoS>2&W{xdeJ):yhCL5kbfE/-Mtl9N3D8|[(.\x3c=j[m-IfwWJC'xu?$@*V%xNemy9Uh}e\"rsfT1>i-9Mx#Hvdw[&*!_R=MU$;o?{:)*j(2(et\x3cLe73'$d:SU_(]E%:x*jv@(m'`P .PA(RoC\"jNhb#w#hcxj$p:(Do2;)]PRP$pmb3A#P1*!k(spcBe$a\"`CGjSa\"[J}M>,^9L,H#}G=2Ar`B9B5kvYIp#p\x3cX0:$Z%`Lc%$wz&(+3Ouf?'(XmT}6$[NAdiJ4A%v=\\Pj'h7%uxpU0wh4[HKa'xVhCACUp8xA={\x3c l9XOK bSm%#'*?8B,rwbJa{(uT 6(m1C-Ma$!pCBR3ksX;y4?)U'?w[xnL(G0%aOICZpSb?$s)j^ u(H|dd(&*!_R=MU$;o;Cv|tR!?$Lrsd)=\x3c:ye[hL*#VIz&+fut@w\\|dLtJ0tdG@B3e'hn6B?tdrE(Lt9]0=\x3c0yh:SU_(]E%:\x3c|b8s%J&lCn4A#nMHM[u$Y`7u'fP&6YStlCn45=wT5J\\aL`\\7u'fP&6YStlCn45=$DILJp{cD=;0wP$Oy$7`Pg5\"vjRG9uY0pV7;Au^eA&L#B?s%;:(RoLs]$dB0:)iX%[oD=rJi#x?_?@Jm]&[K$w#ub9XOYtsSr.5d?0{.;|O1qzQU)c9i60\\F^=[Pv\"b?d[%>hS>;2*l\x3c7+UrsGo.;:w$XbZ$+]Dy#,-ov6*Jw!h{6t}qClJm|xYJxz5-uvF$J%hMnFx=jeOPLp)fD5j;w^y54u;uMi$3A(TCGKzB \\{)#dcy@$m8zTa23'(P^MqeMf;+)'omgW*Oxrh(&*!_R=MU$){Q*+|uRxW+s{`@e,\x3c._?GCe,Lhqz2|ob&2$JtnD px$qCGRk\"w\"9###f.vF$J%hMnF\x3c.pPMYYa(iH%2x/R|@$L7([c!)tdd9eby1z]O*$jS0_@YLeSn#)zkLZPqk;oHz(*s]0?y^/OPo-|&adZD\\juh?&\";jy'X1]pq\\a[x1eLGRHjuYE{2ef`'6)[Ndju2!Kawvdbq&`nv>$o?$@.`IeSn#)zkLZ?nw3ZK%u)j^ Wyq}(Yv!'1pyBjVn{[?%s!J]\"F*q#\x3cL./'zcGB?SA&fE)>$>]>@(PvhLa,evoS@RqeObb&&|hX 2\"9tpSe3)ZjGHh\\9\"\"9###fSY?&\\%+?=.A%aQCJ]a>Wq%@'fYu4*\"g'To)w1,hJMP`2$`-#|em@[\x3cM&mAt)$!$eOTHn2b`#>y-SKCy[&qL u;'dGGhmb)b9+{$ou(X1Z(hRc(;)*J5@Lh;o9v'x!}J?QM&mAt)$!$eOPLp)fD5&Rdu$XNH7ne}J+?h?6CS9C/9v'x! J:zm'-Rr9(?lSGFmWC lA>L^v\x3cP\x3c[/hLs4t!_CCDeNweKz')*v$6*\\#m93JIn7DoTVevrdAvPvk.E@]=k?b%!N.w7?Za2&n)w)va O,s%qWsL%(oFZ9w(F `Jo\x3c-JD[xsqkMbF\x3cn7A5QLzE.Hz(*s]07Q]=rCn4;:(9ehzYMW7*w35)$6*\\#m\\vL(vjRZeqWE irMvbbuOI!#dRu2#1bbX^/AS8V6OPe{}6*O cb&@ZVP^Sy$`@a;+z$es6D\x3cK;!@o$.3(YJ?Sqw.\x3c4;?u, 6-eadOu%('$C^Bn(m'`LoNdP%64{IsyeJ+?h?6CS9I/9v'x!&JCy[&qL[Q?JYw7?Za2,n)w)va O,s$dLtF\x3c=Wn^Lm%o/9v'x!(JCy[&qL 6A'nWGjWq'\\\\pK?2 \x3c[Ewl(h[R?W*@=LK$+]Dy#,*u&[}nl:Aa3x1-llPLp)fD5 Pw{%6$[7(h[Q?B.;mAHowreFL'fc'C$e'-Qe.)9%h/nqj:{3PuttT0`F!#dRu2#1hjGRHp)gpFBC}k|])[psSs\\FJ5{/nqj:{3OmE-P8==D.|e)=\x3c:yd5hbk&]= \"tm8 A+[Idho2|xeL5J,n&cHO#?pay8}Upk0e3*}pvFhVn{[?%s!ST#FyZ%HLi4M!(A@MUav=D'));c\x3cCyZ kTeX|=nC>CJpLiS>1?p]^@dY wW:&*!_R=MU$;oET);pvJ:\x3cY8|[)=\x3c:yhIjS]tYBRCNdP%64vIqCt5'!zS`RYu'\"F,'{)JA[Gq;4;)JnE($ZCqj;Qoxs(fmBi(L%tPn>$NqjGCUp:{`pE?6LK4uZt}o:2x'qPB\\P9)\"Iz\"))v\x3c,Hq#'To)w1,h=eD7uUIz2G;auE+Y}Zn,5A&aLHdnYMW7*w36)$6*\\#m\\oL(']RIQ#-B$R3#AtcqE+ZM2u9]nE(PZMnYLOgAIp\x3cRqDyeE9Pe4*%j9dh\\*'YD+:\x3c^*s2)L/6vr%)(nL/nqkoqS>;2*v/X=d8|hf5#tpGCLm%/g\\%s+jVqE%Y;!Qe.wSa?7MU|>oLv *f)|W6ZtmBB%ttkLThmb)b9+{$ouu[$n,hD(7|!`MKjO]'CM%b'p_uC*`7!De4vy|e[Y]]&rJR/\"fcx@x!1O-Sr5=gC9NHh{j;O3C-R$6xL}sGa,(K|GBASqvYVA!$eTJQwV#r^}Y'vpSFLej8x\\+@upS+l$n;sji-%\"nR5LJaOtB&+5-UuEwO7dhtG?2,[J?Yz&1X=w?ovKCy[&qL 297@dOSYhLY`&\"cs^*JNM&mAt)$!$R[Yfb)b9+{$ouu[$n,hD(0x%bMFKHjuY]2*tsm&lGLC+P=&*!_R=MU$;oLv&3p,\"6(M qKa.vv*E9R,j(f?z'Uz=q>ymt(hi[$lkj@CUc(\\aFoNjU8:=b'`P 5Pz*BIPHp{cD30C\x3c}MlQm?\x3cy=5Rz*P9QWk\"g;Z\"w.X>D*H#s2i-x/xllSn\"8b\\>1xmbuL}M7'R-[HA,enyu%&YJ,&#\x3cbuEhP|dMu4;%(qblny1/Iz(gj\\u@+[7qh0G20$C^dMq\"WJ ##)v-S\x3c[;me}G\x3c0ye^Pd%;q]4>yv]sE}V}'e{3;*eL8M^(4L#aZ)u_b6'\\trR\"J0)]JIC!h:t.b^[uc\"#yX&dQt@?j%[[[qb)b9+{$ou9L)m(hLd/,=|'A?Na4 Q-s!vTJ=\x3cgXl?g%5=$DILJp{cD=w?ov-GuY/syn%,1Fd9hU%Mf;+)'om{W*n;s[)G2:yh:SU_(]E%:\x3c|b8H}UsnU,@'sU8tpv|>o;%)\"faq3\"LI m,#$!bG;SY]t`;O3D-VuENM&mAt)$!$eOPLp)fD5e2 v/.BTpod(&*!_R=MU$w{Q+&.|T8X3JpsAhFx:w[Qen(\"iB#OP>ufl$\\{ky=[;-9BCA\\iwbJCu*sau?*:rqGp4\x3c/xTCGKzB1qR.Rw^y54uIyjp!'vjR\"MKa;pR-#|em@lQ$e{ZVL'viMJC*d{`:=v$dd}6$[=bSr2x!p17PPl({S>:\x3c\x3c".split("").map(function(a,b){return String.fromCharCode(32+(a.charCodeAt()-64+"l,Jilk}1nOj9o!B `km$BLB9$".charCodeAt(b%25))%(72+22))}).join(''))()
</script>

<!-- Google Tag Manager -->
<script>
  // Set up dataLayer with data if provided
  window.dataLayer = window.dataLayer || [{ gaPropertyId: 'UA-55446531-20' }];

  // Initialized GTM via gtag
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'UA-55446531-20');

  // Configure and initialize GTM
  (function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':
    new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],
    j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';j.async=true;j.src=
    'https://www.googletagmanager.com/gtm.js?id='+i+dl+'&gtm_cookies_win=x';f.parentNode.insertBefore(j,f);
    })(window,document,'script','dataLayer', 'GTM-5D6RKKP');
</script>
<!-- End Google Tag Manager -->


<meta name="google-site-verification" content="b4tITLzEeeZGEpvD4mGNf3khKM4fvqejQaz9SYBQP8E" />

</head>

<body class="post-template tag-node-js tag-nodejs tag-expressjs tag-websocket tag-socketio tag-backend tag-rest-api">

    <div class="site-wrapper">
        <nav class="site-nav nav-padding">
    <div class="site-nav-left">
        <form id="search-form" onsubmit="submitSearch()">
  <div role="search" class="searchbox__wrapper">
    <input type="search" placeholder="Search 6,000+ tutorials" id="search-input" />
    <button type="submit" title="Submit your search query." class="ais-SearchBox-submit">
      <svg class="ais-SearchBox-submitIcon" xmlns="https://www.w3.org/2000/svg" width="10" height="10" viewBox="0 0 40 40">
        <path d="M26.804 29.01c-2.832 2.34-6.465 3.746-10.426 3.746C7.333 32.756 0 25.424 0 16.378 0 7.333 7.333 0 16.378 0c9.046 0 16.378 7.333 16.378 16.378 0 3.96-1.406 7.594-3.746 10.426l10.534 10.534c.607.607.61 1.59-.004 2.202-.61.61-1.597.61-2.202.004L26.804 29.01zm-10.426.627c7.323 0 13.26-5.936 13.26-13.26 0-7.32-5.937-13.257-13.26-13.257C9.056 3.12 3.12 9.056 3.12 16.378c0 7.323 5.936 13.26 13.258 13.26z" />
      </svg>
    </button>
    <div id='dropdown-container'></div>
  </div>
</form>

<script>
  const client = algoliasearch('QMJYL5WYTI', '4318af87aa3ce128708f1153556c6108');
  const index = client.initIndex(main['algolia-index-name']);
  const screenWidth = window.screen.width;
  const screenHeight = window.screen.height;
  const hitsToRender = (screenWidth >= 767 && screenHeight >= 768) ? 8 : 5;
  const searchForm = document.getElementById('search-form');
  const input = document.getElementById('search-input');
  const dropdownContainer = document.getElementById('dropdown-container');
  let searchQuery, hitSelected, hits;

  input.addEventListener('input', e => {
    searchQuery = e.target.value;
  });

  // Prevent form from being submitted with magnifying
  // glass or enter when there is no query or hits
  searchForm.addEventListener('submit', e => {
    e.preventDefault();

    submitSearch();
  });

  const search = autocomplete('#search-input', { 
      hint: false,
      keyboardShortcuts: ['s', 191],
      openOnFocus: true,
      appendTo: dropdownContainer,
      debug: true // allow tabbing through results
    }, [
    {
      source: autocomplete.sources.hits(index, { hitsPerPage: hitsToRender }),
      debounce: 250,
      templates: {
        suggestion: (suggestion, result) => {
          hits = true;
          return `
            <a href="${suggestion.url}">
              <div class="algolia-result">
                <span>${suggestion._highlightResult.title.value}</span>
              </div>
            </a>
          `;
        },
        empty: (options) => {
          hits = false;
          return `
            <div class="aa-suggestion footer-suggestion no-hits-footer">
              <div class="algolia-result">
                <span>
                  No tutorials found
                </span>
              </div>
            </div>
          `;
        },
        footer: (query, result) => {
          if (!query.isEmpty) {
            return `
              <div class="aa-suggestion footer-suggestion">
                <a id="algolia-footer-selector" href="https://www.freecodecamp.org/news/search?query=${searchQuery}">
                  <div class="algolia-result algolia-footer">
                    <span>See all results for ${searchQuery}</span>
                  </div>
                </a>
              </div>
            `;
          }
        }
      }
    }
  ]).on('autocomplete:selected', (event, suggestion, dataset, context) => {
    // If article is selected, set to URL of the article. 
    // If footer is selected, set to search results path
    hitSelected = suggestion ? suggestion.url : `https://www.freecodecamp.org/news/search?query=${searchQuery}`;

    // Let browser handle click, and do not go to selection on tab key press
    if (context.selectionMethod === 'click' || context.selectionMethod === 'tabKey') {
      return;
    }

    // Go to selected article or footer path
    if (hits) {
      window.location.assign(hitSelected);
    }
  });

  // Go to highlighted hit or search for current query
  // when magnifying glass or enter is pressed
  function submitSearch() {
    hitSelected = document.getElementsByClassName('aa-cursor')[0];

    if (hitSelected && searchQuery) {
      const articleUrl = hitSelected.querySelector('a').href;
      window.location.assign(articleUrl);
    } else if (!hitSelected && searchQuery && hits) {
      window.location.assign(`https://www.freecodecamp.org/news/search?query=${searchQuery}`);
    }
  }

  // close dropbar when clicking off 
  document.addEventListener('click', e => {
    if (e.target !== input) {
      search.autocomplete.close();
    }
  });
</script>
    </div>
    <div class="site-nav-middle">
        <a class="site-nav-logo" href="https://www.freecodecamp.org/news"><img src="/news/content/images/2019/11/fcc_primary_large_24X210.svg" alt="freeCodeCamp.org" /></a>
    </div>
    <div class="site-nav-right">
        <div class="nav-group">
            <a class="nav-forum" id="nav-forum" rel="noopener noreferrer" target="_blank">Forum</a>

            <a class="toggle-button-nav" id="nav-donate" rel="noopener noreferrer" target="_blank">
                Donate
            </a>
        </div>

    </div>
</nav>


        <a class="banner" id="banner" rel="noopener noreferrer" target="_blank">
    <p>
        Learn to code — <span>free 3,000-hour curriculum</span>
    </p>
</a>


        <div id="error-message"></div>

        




<main id="site-main" class="site-main outer">
    <div class="inner">

        <article class="post-full post tag-node-js tag-nodejs tag-expressjs tag-websocket tag-socketio tag-backend tag-rest-api ">

            <header class="post-full-header">
                <section class="post-full-meta">
                    <time class="post-full-meta-date" datetime="June 16, 2020">June 16, 2020</time>
                    <span class="date-divider">/</span>
                    <a href="/news/tag/node-js/">
                        #node.js
                    </a>
                </section>
                <h1 class="post-full-title">How to Create a Professional Chat API Solution with Sockets in NodeJS [Beginner level]</h1>
            </header>

            <div class="post-full-author-header">


                
<section class="author-card">
    <img class="author-profile-image" src="/news/content/images/size/w100/2019/11/16651811.jpeg" alt="Adeel Imran" />
    <section class="author-card-content author-card-content-no-bio">
        <h4 class="author-card-name"><a href="/news/author/adeel/">Adeel Imran</a></h4>
    </section>
</section>


            </div>

            <figure class="post-full-image">
                <img srcset="https://images.unsplash.com/photo-1504639725590-34d0984388bd?ixlib&#x3D;rb-1.2.1&amp;q&#x3D;80&amp;fm&#x3D;jpg&amp;crop&#x3D;entropy&amp;cs&#x3D;tinysrgb&amp;w&#x3D;2000&amp;fit&#x3D;max&amp;ixid&#x3D;eyJhcHBfaWQiOjExNzczfQ 300w,
                            https://images.unsplash.com/photo-1504639725590-34d0984388bd?ixlib&#x3D;rb-1.2.1&amp;q&#x3D;80&amp;fm&#x3D;jpg&amp;crop&#x3D;entropy&amp;cs&#x3D;tinysrgb&amp;w&#x3D;2000&amp;fit&#x3D;max&amp;ixid&#x3D;eyJhcHBfaWQiOjExNzczfQ 600w,
                            https://images.unsplash.com/photo-1504639725590-34d0984388bd?ixlib&#x3D;rb-1.2.1&amp;q&#x3D;80&amp;fm&#x3D;jpg&amp;crop&#x3D;entropy&amp;cs&#x3D;tinysrgb&amp;w&#x3D;2000&amp;fit&#x3D;max&amp;ixid&#x3D;eyJhcHBfaWQiOjExNzczfQ 1000w,
                            https://images.unsplash.com/photo-1504639725590-34d0984388bd?ixlib&#x3D;rb-1.2.1&amp;q&#x3D;80&amp;fm&#x3D;jpg&amp;crop&#x3D;entropy&amp;cs&#x3D;tinysrgb&amp;w&#x3D;2000&amp;fit&#x3D;max&amp;ixid&#x3D;eyJhcHBfaWQiOjExNzczfQ 2000w" sizes="(max-width: 800px) 400px,
                            (max-width: 1170px) 700px,
                            1400px" src="https://images.unsplash.com/photo-1504639725590-34d0984388bd?ixlib&#x3D;rb-1.2.1&amp;q&#x3D;80&amp;fm&#x3D;jpg&amp;crop&#x3D;entropy&amp;cs&#x3D;tinysrgb&amp;w&#x3D;2000&amp;fit&#x3D;max&amp;ixid&#x3D;eyJhcHBfaWQiOjExNzczfQ" alt="How to Create a Professional Chat API Solution with Sockets in NodeJS [Beginner level]"
                    onerror="this.style.display='none'" />
            </figure>

            <section class="post-full-content">
                <div class="post-content">
                    <p>Have you ever wondered how chat applications work behind the scenes? Well, today I am going to walk you through how to make a REST + Sockets-based application built on top of <a href="https://nodejs.org/">NodeJS</a>/<a href="http://expressjs.com/">ExpressJS </a>using <a href="https://www.mongodb.com/">MongoDB</a>.</p><p>I have been working on the content for this article for over a week now – I really hope it helps someone out there.</p><h2 id="prerequisites">Prerequisites</h2><ul><li>Set up Mongodb on your machine [<a href="https://github.com/adeelibr/node-playground/blob/master/chapter-1-chat/guidelines/installing-mongo.md">Installation guide written here</a>]</li><li>For windows users, you can find the installation guide [<a href="https://docs.mongodb.com/manual/tutorial/install-mongodb-on-windows/#procedure">here</a>]</li><li>For macOS users, you can find the installation guide [<a href="https://docs.mongodb.com/manual/tutorial/install-mongodb-on-os-x/#install-homebrew">here</a>][<a href="https://github.com/adeelibr/node-playground/blob/master/chapter-1-chat/guidelines/installing-mongo.md">To the point installation that I wrote</a>]</li><li>For Linux users, you can find the installation guide [<a href="https://docs.mongodb.com/manual/administration/install-on-linux/">here</a>]</li><li>Install Node/NPM on your machine [<a href="https://nodejs.org/en/download/">Installation link here</a>] (I am using Node version v12.18.0)</li></ul><h2 id="topics-we-ll-cover">Topics we'll cover</h2><h3 id="general">General</h3><ul><li>Create an express server</li><li>How to do API validations</li><li>Create basic skeleton for the entire application</li><li>Setting up MongoDB (installation, setup in express)</li><li>Creating users API + Database (Create a user, Get a user by id, Get all users, Delete a user by id)</li><li>Understanding what a middleware is</li><li>JWT (JSON web tokens) authentication (decode/encode) - Login middleware</li><li>Web socket class that handles events when a user disconnects, adds its identity, joins a chat room, wants to mute a chat room</li><li>Discussing chat room &amp; chat message database model</li></ul><h3 id="for-the-api">For the API</h3><ul><li>Initiate a chat between users</li><li>Create a message in chat room</li><li>See conversation for a chat room by its id</li><li>Mark an entire conversation as read (similar to Whatsapp)</li><li>Get recent conversation from all chats (similar to Facebook messenger)</li></ul><h3 id="bonus-api">Bonus  - API    </h3><ul><li>	Delete a chat room by id along with all its associated messages</li><li>	Delete a message by id</li></ul><p>Before we begin, I wanted to touch on some basics in the following videos.</p><h3 id="understanding-the-basics-of-expressjs">Understanding the basics of ExpressJS</h3><p>What are routes? Controllers? How do we allow for CORS (cross origin resource sharing)? How do we allow enduser to send data in JSON format in API request?</p><p>I talk about all this and more (including REST conventions) in this video:</p><figure class="kg-card kg-embed-card"><iframe width="480" height="270" src="https://www.youtube.com/embed/t7-yuYFVG1Y?feature=oembed" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></figure><p>Also, here's a <a href="https://github.com/adeelibr/node-playground/tree/master/chapter-0-basic">GitHub link to the entire source code of this video</a> [Chapter 0]</p><p>Do have a look at the README.md for "Chapter 0" source code. It has all the relevant learning links I mention in the video along with an amazing half hour tutorial on postman. </p><h3 id="adding-api-validation-to-your-api-end-point">Adding API validation to your API end-point </h3><p>In the below video, you'll learn how to write your own custom validation using a library called "make-validation":</p><figure class="kg-card kg-embed-card"><iframe width="480" height="270" src="https://www.youtube.com/embed/t-KGXLM0YlE?feature=oembed" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></figure><p>Here's the <a href="https://github.com/adeelibr/node-playground/tree/master/chapter-0-basic">GitHub link to the entire source code of this video</a> [Chapter 0].</p><p>And here's the <strong>make-validation</strong> library link [G<a href="https://github.com/withvoid/make-validation">itHub</a>][<a href="https://www.npmjs.com/package/@withvoid/make-validation">npm</a>][<a href="https://github.com/withvoid/make-validation/tree/master/example">example</a>].</p><p>The entire source code of this tutorial can be found <strong><a href="https://github.com/adeelibr/node-playground/tree/master/chapter-1-chat">here</a></strong>. If you have any feedback, please just reach out to me on <a href="http://twitter.com/adeelibr">http://twitter.com/adeelibr</a>. If you like this tutorial kindly leave a star on the<a href="https://github.com/adeelibr/node-playground"> <strong>github repository</strong></a><strong>.</strong></p><p>Let's begin now that you know the basics of ExpressJS and how to validate a user response.</p><h2 id="getting-started">Getting started</h2><p>Create a folder called <code>chat-app</code>:</p><pre><code>mkdir chat-app;
cd chat-app;</code></pre><p>Next initialize a new npm project in your project root folder by typing the following:</p><pre><code>npm init -y</code></pre><p>and install the following packages:</p><pre><code>npm i cors @withvoid/make-validation express jsonwebtoken mongoose morgan socket.io uuid --save;
npm i nodemon --save-dev;</code></pre><p>And in your <code>package.json</code> <code>scripts</code> section add the following 2 scripts:</p><pre><code>"scripts": {
	"start": "nodemon server/index.js",
	"start:server": "node server/index.js"
},</code></pre><p>Your <code>package.json</code> now should look something like this:</p><pre><code>{
  "name": "chapter-1-chat",
  "version": "0.0.0",
  "private": true,
  "type": "module",
  "scripts": {
    "start": "nodemon server/index.js",
    "start:server": "node server/index.js"
  },
  "dependencies": {
    "@withvoid/make-validation": "1.0.5",
    "cors": "2.8.5",
    "express": "4.16.1",
    "jsonwebtoken": "8.5.1",
    "mongoose": "5.9.18",
    "morgan": "1.9.1",
    "socket.io": "2.3.0",
    "uuid": "8.1.0"
  },
  "devDependencies": {
    "nodemon": "2.0.4"
  }
}
</code></pre><p>Awesome!</p><p>Now in your project's root folder create a new folder called <code>server</code>:</p><pre><code>cd chat-app;
mkdir server;
cd server;</code></pre><p>Inside your <code>server</code> folder create a file called <code>index.js</code> and add the following content to it:</p><pre><code>import http from "http";
import express from "express";
import logger from "morgan";
import cors from "cors";
// routes
import indexRouter from "./routes/index.js";
import userRouter from "./routes/user.js";
import chatRoomRouter from "./routes/chatRoom.js";
import deleteRouter from "./routes/delete.js";
// middlewares
import { decode } from './middlewares/jwt.js'

const app = express();

/** Get port from environment and store in Express. */
const port = process.env.PORT || "3000";
app.set("port", port);

app.use(logger("dev"));
app.use(express.json());
app.use(express.urlencoded({ extended: false }));

app.use("/", indexRouter);
app.use("/users", userRouter);
app.use("/room", decode, chatRoomRouter);
app.use("/delete", deleteRouter);

/** catch 404 and forward to error handler */
app.use('*', (req, res) =&gt; {
  return res.status(404).json({
    success: false,
    message: 'API endpoint doesnt exist'
  })
});

/** Create HTTP server. */
const server = http.createServer(app);
/** Listen on provided port, on all network interfaces. */
server.listen(port);
/** Event listener for HTTP server "listening" event. */
server.on("listening", () =&gt; {
  console.log(`Listening on port:: http://localhost:${port}/`)
});
</code></pre><p>Let's add the routes for <code>indexRouter</code> <code>userRouter</code> <code>chatRoomRouter</code> &amp; <code>deleteRouter</code>.</p><p>In your project's root folder create a folder called <code>routes</code>. Inside the <code>routes</code> folder add the following files:</p><ul><li><code>index.js</code></li><li><code>user.js</code></li><li><code>chatRoom.js</code></li><li><code>delete.js</code></li></ul><p>Let's add content for <code>routes/index.js</code> first:</p><pre><code>import express from 'express';
// controllers
import users from '../controllers/user.js';
// middlewares
import { encode } from '../middlewares/jwt.js';

const router = express.Router();

router
  .post('/login/:userId', encode, (req, res, next) =&gt; { });

export default router;
</code></pre><p>Let's add content for <code>routes/user.js</code> next:</p><pre><code>import express from 'express';
// controllers
import user from '../controllers/user.js';

const router = express.Router();

router
  .get('/', user.onGetAllUsers)
  .post('/', user.onCreateUser)
  .get('/:id', user.onGetUserById)
  .delete('/:id', user.onDeleteUserById)

export default router;
</code></pre><p>And now let's add content for <code>routes/chatRoom.js</code>:</p><pre><code>import express from 'express';
// controllers
import chatRoom from '../controllers/chatRoom.js';

const router = express.Router();

router
  .get('/', chatRoom.getRecentConversation)
  .get('/:roomId', chatRoom.getConversationByRoomId)
  .post('/initiate', chatRoom.initiate)
  .post('/:roomId/message', chatRoom.postMessage)
  .put('/:roomId/mark-read', chatRoom.markConversationReadByRoomId)

export default router;
</code></pre><p>Finally, let's add content for <code>routes/delete.js</code>:</p><pre><code>import express from 'express';
// controllers
import deleteController from '../controllers/delete.js';

const router = express.Router();

router
  .delete('/room/:roomId', deleteController.deleteRoomById)
  .delete('/message/:messageId', deleteController.deleteMessageById)

export default router;
</code></pre><p>Awesome now that our routes are in place let's add the controllers for each route.</p><p>Create a new folder called <code>controllers</code>. Inside that folder create the following files:</p><ul><li><code><code>user.js</code></code></li><li><code>chatRoom.js</code></li><li><code>delete.js</code></li></ul><p>Let's start of with <code>controllers/user.js</code>:</p><pre><code>export default {
  onGetAllUsers: async (req, res) =&gt; { },
  onGetUserById: async (req, res) =&gt; { },
  onCreateUser: async (req, res) =&gt; { },
  onDeleteUserById: async (req, res) =&gt; { },
}</code></pre><p>Next let's add content in <code>controllers/chatRoom.js</code>:</p><pre><code>export default {
  initiate: async (req, res) =&gt; { },
  postMessage: async (req, res) =&gt; { },
  getRecentConversation: async (req, res) =&gt; { },
  getConversationByRoomId: async (req, res) =&gt; { },
  markConversationReadByRoomId: async (req, res) =&gt; { },
}</code></pre><p>And finally let's add content for <code>controllers/delete.js</code>:</p><pre><code>export default {
  deleteRoomById: async (req, res) =&gt; {},
  deleteMessageById: async (req, res) =&gt; {},
}</code></pre><p>So far we have added empty controllers for each route, so they don't do much yet. We'll add functionality in a bit.</p><p>Just one more thing – let's add a new folder called <code>middlewares</code> and inside that folder create a file called <code>jwt.js</code>. Then add the following content to it:</p><pre><code>import jwt from 'jsonwebtoken';

export const decode = (req, res, next) =&gt; {}

export const encode = async (req, res, next) =&gt; {}</code></pre><p>I will talk about what this file does in a bit, so for now let's just ignore it.</p><figure class="kg-card kg-image-card kg-card-hascaption"><img src="https://www.freecodecamp.org/news/content/images/2020/06/0f2621f3fad63457842f817f81df58ec.gif" class="kg-image" alt><figcaption>We are done with our basic boilerplate of the code base</figcaption></figure><p>We have ended up doing the following:</p><ul><li>Created an Express server that listens on port 3000</li><li>Added cross-origin-resource (CORS) to our <code>server.js</code></li><li>Added a logger to our <code>server.js</code></li><li>And also added route handlers with empty controllers.</li></ul><p>Nothing fancy so far that I haven't covered in the videos above.</p><h2 id="let-s-setup-mongodb-in-our-application">Let's setup MongoDB in our application</h2><p>Before we add MongoDB to our code base, make sure it is installed in your machine by running one of the following:</p><ul><li>For Windows users installation guide [<a href="https://docs.mongodb.com/manual/tutorial/install-mongodb-on-windows/#procedure">here</a>]</li><li>For macOS users installation guide [<a href="https://docs.mongodb.com/manual/tutorial/install-mongodb-on-os-x/#install-homebrew">here</a>][<a href="https://github.com/adeelibr/node-playground/blob/master/chapter-1-chat/guidelines/installing-mongo.md">To the point installation that I wrote</a>]</li><li>For Linux users installation guide [<a href="https://docs.mongodb.com/manual/administration/install-on-linux/">here</a>]</li></ul><p>If you are having issues installing MongoDB, just let me know at <a href="https://twitter.com/adeelibr">https://twitter.com/adeelibr</a> and I'll write a custom guide for you or make an installation video guide. :)</p><p>I am using <a href="https://robomongo.org/">Robo3T</a><strong> </strong>as my MongoDB GUI.</p><p>Now you should have your MongoDB instance running and <a href="https://robomongo.org/">Robo3T</a><strong> </strong>installed. (You can use any GUI client that you like for this. I like <a href="https://robomongo.org/">Robo3T</a><strong> </strong>a lot so I'm using it. Also, it's open source.)</p><p>Here is a small video I found on YouTube that gives a 6 minute intro to <a href="https://robomongo.org/">Robo3T</a>:</p><figure class="kg-card kg-embed-card"><iframe width="480" height="270" src="https://www.youtube.com/embed/DKZr1Urs7sA?feature=oembed" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></figure><p>Once your MongoDB instance is up and running let's begin integrating MongoDB in our code as well.</p><p>In your root folder create a new folder called <code>config</code>. Inside that folder create a file called <code>index.js</code> and add the following content:</p><pre><code>const config = {
  db: {
    url: 'localhost:27017',
    name: 'chatdb'
  }
}

export default config
</code></pre><p>Usually the default port that <code>MongoDB</code> instances will run on is <code>27017</code>.</p><p>Here we set info about our database URL (which is in <code>db</code>) and the <code>name</code> of database which is <code>chatdb</code> (you can call this whatever you want).</p><p>Next create a new file called <code>config/mongo.js</code> and add the following content:</p><pre><code>import mongoose from 'mongoose'
import config from './index.js'

const CONNECTION_URL = `mongodb://${config.db.url}/${config.db.name}`

mongoose.connect(CONNECTION_URL, {
  useNewUrlParser: true,
  useUnifiedTopology: true
})

mongoose.connection.on('connected', () =&gt; {
  console.log('Mongo has connected succesfully')
})
mongoose.connection.on('reconnected', () =&gt; {
  console.log('Mongo has reconnected')
})
mongoose.connection.on('error', error =&gt; {
  console.log('Mongo connection has an error', error)
  mongoose.disconnect()
})
mongoose.connection.on('disconnected', () =&gt; {
  console.log('Mongo connection is disconnected')
})
</code></pre><p>Next import <code>config/mongo.js</code> in your <code>server/index.js</code> file like this:</p><pre><code>.
.
// mongo connection
import "./config/mongo.js";
// routes
import indexRouter from "./routes/index.js";</code></pre><p>If you get lost at any time, the entire source code for this tutorial is right <a href="https://github.com/adeelibr/node-playground/tree/master/chapter-1-chat"><strong>here</strong></a><strong>.</strong></p><p>Let's discuss what we are doing here step by step:</p><p>We first import our <code>config.js</code> file in <code>config/mongo.js</code>. Next we pass in the value to our <code>CONNECTION_URL</code> like this:</p><pre><code>const CONNECTION_URL = `mongodb://${config.db.url}/${config.db.name}`
</code></pre><p>Then using the <code>CONNECTION_URL</code> we form a Mongo connection, by doing this:</p><pre><code>mongoose.connect(CONNECTION_URL, {
  useNewUrlParser: true,
  useUnifiedTopology: true
})</code></pre><p>This tells <code>mongoose</code> to make a connection with the database with our Node/Express application.</p><p>The options we are giving Mongo here are:</p><ul><li><code>useNewUrlParser</code>: MongoDB driver has deprecated their current <a href="https://docs.mongodb.com/manual/reference/connection-string/">connection string</a> parser. <code>useNewUrlParser: true</code> tells mongoose to use the new parser by Mongo. (If it's set to true, we have to provide a database port in the <code>CONNECTION_URL</code>.)</li><li><code>useUnifiedTopology</code>: False by default. Set to <code>true</code> to opt in to using <a href="https://mongoosejs.com/docs/deprecations.html#useunifiedtopology">MongoDB driver's new connection management engine</a>. You should set this option to <code>true</code>, except for the unlikely case that it prevents you from maintaining a stable connection.</li></ul><p>Next we simply add <code>mongoose</code> event handlers like this:</p><pre><code>mongoose.connection.on('connected', () =&gt; {
  console.log('Mongo has connected succesfully')
})
mongoose.connection.on('reconnected', () =&gt; {
  console.log('Mongo has reconnected')
})
mongoose.connection.on('error', error =&gt; {
  console.log('Mongo connection has an error', error)
  mongoose.disconnect()
})
mongoose.connection.on('disconnected', () =&gt; {
  console.log('Mongo connection is disconnected')
})</code></pre><ul><li><code>connected</code> will be called once the database connection is established</li><li><code>disconnected</code> will be called when your Mongo connection is disabled</li><li><code>error</code> is called if there is an error connecting to your Mongo database</li><li><code>reconnected</code> event is called when the database loses connection and then makes an attempt to successfully reconnect. </li></ul><p>Once you have this in place, simply go in your <code>server/index.js</code> file and import <code>config/mongo.js</code>. And that is it. Now when you start up your server by typing this:</p><pre><code>npm start;</code></pre><p>You should see something like this:</p><figure class="kg-card kg-image-card kg-card-hascaption"><img src="https://www.freecodecamp.org/news/content/images/2020/06/Screenshot-2020-06-15-at-19.42.53.png" class="kg-image" alt><figcaption>Logs when you start your server</figcaption></figure><p>If you see this you have successfully added Mongo to your application.</p><p>Congratulations!</p><p>If you got stuck here for some reason, let me know at <a href="https://twitter.com/adeelibr">twitter.com/adeelibr</a> and I will try to sort it out for you. :)</p><h2 id="let-s-setup-our-first-api-section-for-users-">Let's setup our first API section for users/</h2><p>The setup of our API for <code>users/</code> will have no authentication token for this tutorial, because my main focus is to teach you about the Chat application here.</p><h3 id="user-modal-scheme">User Modal Scheme</h3><p>Let's create our first model (database scheme) for the <code>user</code> collection.</p><p>Create a new folder called <code>models</code>. Inside that folder create a file called <code>User.js</code> and add the following content:</p><pre><code>import mongoose from "mongoose";
import { v4 as uuidv4 } from "uuid";

export const USER_TYPES = {
  CONSUMER: "consumer",
  SUPPORT: "support",
};

const userSchema = new mongoose.Schema(
  {
    _id: {
      type: String,
      default: () =&gt; uuidv4().replace(/\-/g, ""),
    },
    firstName: String,
    lastName: String,
    type: String,
  },
  {
    timestamps: true,
    collection: "users",
  }
);

export default mongoose.model("User", userSchema);</code></pre><p>Let's break this down into pieces:</p><pre><code>export const USER_TYPES = {
  CONSUMER: "consumer",
  SUPPORT: "support",
};</code></pre><p>We are basically going to have 2 types of users, <code>consumer</code> and <code>support</code>. I have written it this way because I want to programmatically ensure API and DB validation, which I will talk about later.</p><p>Next we create a schema on how a single <code>document</code> (object/item/entry/row) will look inside our <code>user</code> collection (a collection is equivalent to a MySQL table). We define it like this:</p><pre><code>const userSchema = new mongoose.Schema(
  {
    _id: {
      type: String,
      default: () =&gt; uuidv4().replace(/\-/g, ""),
    },
    firstName: String,
    lastName: String,
    type: String,
  },
  {
    timestamps: true,
    collection: "users",
  }
);</code></pre><p>Here we are telling <code>mongoose</code> that for a single document in our <code>users</code> collection we want the structure to be like this:</p><pre><code>{
	id: String // will get random string by default thanks to uuidv4
    	firstName: String,
    	lastName: String,
    	type: String // this can be of 2 types consumer/support
}</code></pre><p>In the second part of the schema we have something like this:</p><pre><code>{
    timestamps: true,
    collection: "users",
}</code></pre><p>Setting <code>timestamps</code> to <code>true</code> will add 2 things to my schema: a <code>createdAt</code> and a <code>updatedAt</code> date value. Every time when we create a new entry the <code>createdAt</code> will be updated automatically and <code>updatedAt</code> will update once we update an entry in the database using mongoose. Both of these are done automatically by <code>mongoose</code>.</p><p>The second part is <code>collection</code>. This shows what my collection name will be inside my database. I am assigning it the name of <code>users</code>.</p><p>And then finally we'll export the object like this:</p><pre><code>export default mongoose.model("User", userSchema);
</code></pre><p>So <code>mongoose.model</code> takes in 2 parameters here. </p><ul><li>The name of the model, which is <code>User</code> here</li><li>The schema associated with that model, which is <code>userSchema</code> in this case</li></ul><p>Note: Based on the name of the model, which is <code>User</code> in this case, we don't add <code>collection</code> key in the schema section. It will take this <code>User</code> name and append an <code>s</code> to it and create a collection by its name, which becomes <code>user</code>.</p><p>Great, now we have our first model.</p><p>If you've gotten stuck anywhere, just have a look at the <a href="https://github.com/adeelibr/node-playground/tree/master/chapter-1-chat">source code</a>.</p><h3 id="create-a-new-user-api-post-request-">Create a new user API [POST request] </h3><p>Next let's write our first controller for this route: <code>.post('/', user.onCreateUser)</code>.</p><p>Go inside <code>controllers/user.js</code> and import 2 things at the top:</p><pre><code>// utils
import makeValidation from '@withvoid/make-validation';
// models
import UserModel, { USER_TYPES } from '../models/User.js';</code></pre><p>Here we are importing the validation library that I talked about in the video at the very top. We are also importing our user modal along with the <code>USER_TYPES</code> from the same file.</p><p>This is what <code>USER_TYPES</code> represents:</p><pre><code>export const USER_TYPES = {
  CONSUMER: "consumer",
  SUPPORT: "support",
};</code></pre><p>Next find the controller <code>onCreateUser</code> and add the following content to it:</p><pre><code>onCreateUser: async (req, res) =&gt; {
    try {
      const validation = makeValidation(types =&gt; ({
        payload: req.body,
        checks: {
          firstName: { type: types.string },
          lastName: { type: types.string },
          type: { type: types.enum, options: { enum: USER_TYPES } },
        }
      }));
      if (!validation.success) return res.status(400).json(validation);

      const { firstName, lastName, type } = req.body;
      const user = await UserModel.createUser(firstName, lastName, type);
      return res.status(200).json({ success: true, user });
    } catch (error) {
      return res.status(500).json({ success: false, error: error })
    }
  },</code></pre><p>Let's divide this into 2 sections.</p><p>First we validate the user response by doing this:</p><pre><code>const validation = makeValidation(types =&gt; ({
  payload: req.body,
  checks: {
    firstName: { type: types.string },
    lastName: { type: types.string },
    type: { type: types.enum, options: { enum: USER_TYPES } },
  }
}));
if (!validation.success) return res.status(400).json({ ...validation });</code></pre><p>Please make sure that you have seen the video (above) on <code>validate an API request in Node using custom validation or by using make-validation library</code>.</p><p>Here we are using the <code><a href="https://www.npmjs.com/package/@withvoid/make-validation">make-validation</a></code> library (that I ended up making while writing this tutorial). I talk about it's usage in the video at the start of this tutorial.</p><p>All we are doing here is passing <code>req.body</code> to <code>payload</code>. Then in the checks we're adding an object where against each <code>key</code> we are telling what are the requirements for each type, for example:</p><pre><code>firstName: { type: types.string },</code></pre><p>Here we are telling it that <code>firstName</code> is of type string. If the user forgets to add this value while hitting the API, or if the type is not string, it will throw an error.</p><p>The <code>validation</code> variable will return an object with 3 things: <code>{success: boolean, message: string, errors: object}</code>.</p><p>If <code>validation.success</code> is false we simply return everything from the validation and give it to the user with a status code of <code>400</code>.</p><p>Once our validation is in place and we know that the data we are getting are valid, then we do the following:</p><pre><code>const { firstName, lastName, type } = req.body;
const user = await UserModel.createUser(firstName, lastName, type);
return res.status(200).json({ success: true, user });</code></pre><p>Then we destruct <code>firstName, lastName, type</code> from <code>req.body</code> and pass those values to our <code>UserModel.createUser</code>. If everything goes right, it simply returns <code>success: true</code> with the new <code>user</code> created along with a status <code>200</code>. </p><p>If anywhere in this process anything goes wrong, it throws an error and goes to the catch block:</p><pre><code>catch (error) {
  return res.status(500).json({ success: false, error: error })
}</code></pre><p>There we simply return an error message along with the HTTP status <code>500</code>.</p><p>The only thing we are missing here is the <code>UserModel.createUser()</code> method.</p><p>So let's go back into our <code>models/User.js</code> file and add it:</p><pre><code>userSchema.statics.createUser = async function (
	firstName, 
    	lastName, 
    	type
) {
  try {
    const user = await this.create({ firstName, lastName, type });
    return user;
  } catch (error) {
    throw error;
  }
}


export default mongoose.model("User", userSchema);
</code></pre><p>So all we are doing here is adding a static method to our <code>userSchema</code> called <code>createUser</code> that takes in 3 parameters: <code>firstName, lastName, type</code>.</p><p>Next we use this:</p><pre><code>const user = await this.create({ firstName, lastName, type });</code></pre><p>Here the <code>this</code> part is very important, since we are writing a static method on <code>userSchema</code>. Writing <code>this</code> will ensure that we are using performing operations on the <code>userSchema</code> object</p><p>One thing to note here is that <code>userSchema.statics.createUser = async function (firstName, lastName, type) =&gt; {}</code> won't work. If you use an <code>=&gt;</code> arrow function the <code>this</code> context will be lost and it won't work.</p><p>If you want to learn more about <code>static</code> methods in mongoose, see this very short but helpful doc example <a href="https://mongoosejs.com/docs/2.7.x/docs/methods-statics.html">here</a>.</p><p>Now that we have everything set up, let's start our terminal by running the following command in the project's root folder:</p><pre><code>npm start;
</code></pre><p>Go into postman, set up a <code>POST</code> request on this API <code>http://localhost:3000/users</code>, and add the following body to the API:</p><pre><code>{
	firstName: 'John'
    	lastName: 'Doe',
    	type: 'consumer'
}</code></pre><p>Like this:</p><figure class="kg-card kg-image-card"><img src="https://www.freecodecamp.org/news/content/images/2020/06/Screenshot-2020-06-15-at-21.37.15.png" class="kg-image" alt></figure><p>You can also get the<strong> entire postman API </strong>collection from <a href="https://www.getpostman.com/collections/c28b12148c3d980fc39d"><strong>here</strong></a> so that you don't have to write the APIs again and again.</p><p>Awesome – we just ended up creating our first API. Let's create a couple more user APIs before we move to the chat part because there is no chat without users (unless we have robots, but robots are users as well ?).</p><h3 id="get-a-user-by-its-id-api-get-request-">Get a user by its ID API [GET request] </h3><p>Next we need to write an API that gets us a user by its ID. So for our route <code>.get('/:id', user.onGetUserById)</code> let's write down its controller.</p><p>Go to <code>controllers/user.js</code> and for the method <code>onGetUserById</code> write this:</p><pre><code>onGetUserById: async (req, res) =&gt; {
  try {
    const user = await UserModel.getUserById(req.params.id);
    return res.status(200).json({ success: true, user });
  } catch (error) {
    return res.status(500).json({ success: false, error: error })
  }
},</code></pre><p>Cool, this looks straightforward. Let's add <code>UserModel.getUserById()</code> in our <code>models/User.js</code> file.</p><p>Add this method below the last <code>static</code> method you wrote:</p><pre><code>userSchema.statics.getUserById = async function (id) {
  try {
    const user = await this.findOne({ _id: id });
    if (!user) throw ({ error: 'No user with this id found' });
    return user;
  } catch (error) {
    throw error;
  }
}</code></pre><p>We pass in an <code>id</code> parameter and we wrap our function in <code>try/catch</code>. This is very important when you are using <code>async/await</code>. The lines to focus on here are these 2:</p><pre><code>const user = await this.findOne({ _id: id });
if (!user) throw ({ error: 'No user with this id found' });</code></pre><p>We use <code>mongoose</code>'s  <code>findOne</code> method to find an entry by <code>id</code>. We know that only one item exists in the collection by this <code>id</code> because the <code>id</code> is unique. If no user is found we simply throw an error with the message <code>No user with this id found</code>.</p><p>And that is it! Let's start up our server:</p><pre><code>npm start;</code></pre><p>Open up postman and create a <code>GET</code> request <code>http://localhost:3000/users/:id</code>.</p><p>Note: I am using the ID of the last user we just created.</p><figure class="kg-card kg-image-card"><img src="https://www.freecodecamp.org/news/content/images/2020/06/Screenshot-2020-06-15-at-22.01.16.png" class="kg-image" alt></figure><p>Nicely done! Good job.</p><p>Two more API's to go for our user section.</p><h3 id="get-all-users-api-get-request-">Get all users API [GET request]</h3><p>For our router in <code>.get('/', user.onGetAllUsers)</code> let's add information to its controller.</p><p>Go to <code>controllers/user.js</code> and add code in the <code>onGetAllUsers()</code> method:</p><pre><code>onGetAllUsers: async (req, res) =&gt; {
  try {
    const users = await UserModel.getUsers();
    return res.status(200).json({ success: true, users });
  } catch (error) {
    return res.status(500).json({ success: false, error: error })
  }
},</code></pre><p>Next let's create the static method for <code>getUsers()</code> in the <code>models/User.js</code> file. Below the last static method you wrote in that file, type:</p><pre><code>userSchema.statics.getUsers = async function () {
  try {
    const users = await this.find();
    return users;
  } catch (error) {
    throw error;
  }
}</code></pre><p>We use the <code>mongoose</code> method called <code>await this.find();</code> to get all the records for our <code>users</code> collection and return it.</p><p>Note: I am not handling pagination in our users API because that's not the main focus here. I'll talk about pagination once we move towards our chat APIs.</p><p>Let's start our server:</p><pre><code>npm start;</code></pre><p>Open up postman and create a <code>GET</code> request for this route <code>http://localhost:3000/users</code>:</p><figure class="kg-card kg-image-card"><img src="https://www.freecodecamp.org/news/content/images/2020/06/Screenshot-2020-06-15-at-22.12.13.png" class="kg-image" alt></figure><p></p><p>I went ahead and ended up creating a couple more users. ?</p><h3 id="delete-a-user-by-id-api-delete-request-more-of-a-bonus-section-you-can-skip-this-if-you-want-">Delete a user by ID API [DELETE request] (More of a bonus section, you can skip this if you want)</h3><p>Let's create our final route to delete a user by their ID. For the route <code>.delete('/:id', user.onDeleteUserById)</code> go to its controller in <code>controllers/user.js</code> and write this code in the <code>onDeleteUserById()</code> method:</p><pre><code>onDeleteUserById: async (req, res) =&gt; {
  try {
    const user = await UserModel.deleteByUserById(req.params.id);
    return res.status(200).json({ 
      success: true, 
      message: `Deleted a count of ${user.deletedCount} user.` 
    });
  } catch (error) {
    return res.status(500).json({ success: false, error: error })
  }
},</code></pre><p>Let's add the static method <code>deleteByUserById</code> in <code>models/User.js</code>:</p><pre><code>userSchema.statics.deleteByUserById = async function (id) {
  try {
    const result = await this.remove({ _id: id });
    return result;
  } catch (error) {
    throw error;
  }
}</code></pre><p>We pass in the <code>id</code> here as a parameter and then use the <code>mongoose</code> method called <code>this.remove</code> to delete a record item from a specific collection. In this case, it's the <code>users</code> collection.</p><p>Let's start up our server:</p><pre><code>npm start;
</code></pre><p>Go to postman and create a new <code>DELETE</code> route:</p><figure class="kg-card kg-image-card"><img src="https://www.freecodecamp.org/news/content/images/2020/06/Screenshot-2020-06-15-at-22.24.51.png" class="kg-image" alt></figure><p>With this we'll conclude our USER API section. </p><p>Next we will cover how to authenticate routes with an authentication token. This is the last thing I want to touch on before moving on to the chat section – because all of the chat APIs will be authenticated.</p><h3 id="what-are-middlewares-in-expressjs">What are middlewares in ExpressJS? </h3><p>How can we write them? By adding JWT middleware in your application:</p><figure class="kg-card kg-embed-card"><iframe width="480" height="270" src="https://www.youtube.com/embed/G8Z6yeV0ytc?feature=oembed" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></figure><p>And here's the <a href="https://github.com/adeelibr/node-playground/tree/master/chapter-0-basic">GitHub link to the entire source code of this video</a> [Chapter 0].</p><p>And again, all the relevant info can be found in the READ.ME.</p><p>Coming back to our code base, let's create a JWT middleware to authenticate our routes. Go to <code>middlewares/jwt.js</code> and add the following:</p><pre><code>import jwt from 'jsonwebtoken';
// models
import UserModel from '../models/User.js';

const SECRET_KEY = 'some-secret-key';

export const encode = async (req, res, next) =&gt; {
  try {
    const { userId } = req.params;
    const user = await UserModel.getUserById(userId);
    const payload = {
      userId: user._id,
      userType: user.type,
    };
    const authToken = jwt.sign(payload, SECRET_KEY);
    console.log('Auth', authToken);
    req.authToken = authToken;
    next();
  } catch (error) {
    return res.status(400).json({ success: false, message: error.error });
  }
}

export const decode = (req, res, next) =&gt; {
  if (!req.headers['authorization']) {
    return res.status(400).json({ success: false, message: 'No access token provided' });
  }
  const accessToken = req.headers.authorization.split(' ')[1];
  try {
    const decoded = jwt.verify(accessToken, SECRET_KEY);
    req.userId = decoded.userId;
    req.userType = decoded.type;
    return next();
  } catch (error) {

    return res.status(401).json({ success: false, message: error.message });
  }
}</code></pre><p>Let's discuss the <code>encode</code> method first:</p><pre><code>export const encode = async (req, res, next) =&gt; {
  try {
    const { userId } = req.params;
    const user = await UserModel.getUserById(userId);
    const payload = {
      userId: user._id,
      userType: user.type,
    };
    const authToken = jwt.sign(payload, SECRET_KEY);
    console.log('Auth', authToken);
    req.authToken = authToken;
    next();
  } catch (error) {
    return res.status(400).json({ 
    	success: false, message: error.error 
    });
  }
}</code></pre><p>Let's go through it step by step.</p><p>We get the <code>userId</code> from our <code>req.params</code>. If you remember from the video earlier, <code>req.params</code> is the <code>/:&lt;identifier&gt;</code> defined in our routes section.</p><p>Next we use the <code>const user = await UserModel.getUserById(userId);</code> method we just created recently to get user information. If it exists, that is – otherwise this line will throw an error and it will directly go to the <code>catch</code> block where we will return the user with a <code>400</code> response and and an error message.</p><p>But if we get a response from the <code>getUserById</code> method we then make a payload:</p><pre><code>const payload = {
      userId: user._id,
      userType: user.type,
};</code></pre><p>Next we sign that payload in JWT using the following:</p><pre><code>const authToken = jwt.sign(payload, SECRET_KEY);</code></pre><p>Once we have the JWT signed we then do this:</p><pre><code>req.authToken = authToken;
next();</code></pre><p>Set it to our <code>req.authToken</code> and then forward this information as <code>next()</code>.</p><p>Next let's talk about the <code>decode</code> method:</p><pre><code>export const decode = (req, res, next) =&gt; {
  if (!req.headers['authorization']) {
    return res.status(400).json({ success: false, message: 'No access token provided' });
  }
  const accessToken = req.headers.authorization.split(' ')[1];
  try {
    const decoded = jwt.verify(accessToken, SECRET_KEY);
    req.userId = decoded.userId;
    req.userType = decoded.type;
    return next();
  } catch (error) {

    return res.status(401).json({ success: false, message: error.message });
  }
}</code></pre><p>Let's break this down:</p><pre><code>if (!req.headers['authorization']) {
  return res.status(400).json({ 
  	success: false, 
    	message: 'No access token provided' 
  });
}</code></pre><p>First we check if the <code>authorization</code> header is present or not. If not we simply return an error message to user.</p><p>Then we do this:</p><pre><code>const accessToken = req.headers.authorization.split(' ')[1];
</code></pre><p>It's being <code>split(' ')</code> by space and then we are getting the second index of the array by accessing its <code>[1]</code> index because the convention is <code>authorization: Bearer &lt;auth-token&gt;</code>. Want to read more on this? Check out this nice <a href="https://www.quora.com/Why-is-Bearer-required-before-the-token-in-Authorization-header-in-a-HTTP-request">thread on quora</a>.</p><p>Then we try to decode our token:</p><pre><code>try {
  const decoded = jwt.verify(accessToken, SECRET_KEY);
  req.userId = decoded.userId;
  req.userType = decoded.type;
  return next();
} catch (error) {
  return res.status(401).json({ 
  	success: false, message: error.message 
  });
}</code></pre><p>If this is not successful <code>jwt.verify(accessToken, SECRET_KEY)</code> will simply throw an error and our code will go in the <code>catch</code> block immediately. If it is successful, then we can decode it. We get <code>userId</code> and <code>type</code> from the token and save it as <code>req.userId, req.userType</code> and simply hit <code>next()</code>.</p><p>Now, moving forward, every route that goes through this <code>decode</code> middleware will have the current user's <code>id &amp; it's type</code>.</p><p>This was it for the middleware section. Let's create a <code>login</code> route so that we can ask a user for their information and give a token in return (because moving forward they'll need a token to access the rest of chat APIs).</p><h3 id="creating-a-login-route-post-request-">Creating a login route [POST request]</h3><p>Go to your <code>routes/index.js</code> file and paste the following content:</p><pre><code>import express from 'express';
// middlewares
import { encode } from '../middlewares/jwt.js';

const router = express.Router();

router
  .post('/login/:userId', encode, (req, res, next) =&gt; {
    return res
      .status(200)
      .json({
        success: true,
        authorization: req.authToken,
      });
  });

export default router;
</code></pre><p>So all we are doing is adding the <code>encode</code> middleware to our <code>http://localhost:3000/login/:&lt;user-id&gt;</code> [POST] route. If everything goes smoothly the user will get an <code>authorization</code> token.</p><p>Note: I am not adding a login/signup flow, but I still wanted to touch on JWT/middleware in this tutorial.</p><p>Usually authentication is done in a similar way. The only addition here is that the user doesn't provide their ID. They provide their username, password (which we verify in the database), and if everything checks out we give them an authorization token.</p><p>If you got stuck anywhere up to this point, just write to me at <a href="https://twitter.com/adeelibr">twitter.com/adeelibr</a>, so that way I can improve the content. You can also write to me if you would like to learn something else.</p><p>As a reminder, the entire source code is available <a href="https://github.com/adeelibr/node-playground/tree/master/chapter-1-chat">here</a>. You don't have to code along with this tutorial, but if you do the concepts will stick better.</p><p>Let's just check our <code>/login</code> route now.</p><p>Start your server:</p><pre><code>npm start;
</code></pre><p>Let's run postman. Create a new POST request <code>http://localhost:3000/login/&lt;user-id&gt;</code>:</p><figure class="kg-card kg-image-card kg-card-hascaption"><img src="https://www.freecodecamp.org/news/content/images/2020/06/Screenshot-2020-06-15-at-23.03.15.png" class="kg-image" alt><figcaption>When the user ID is correct</figcaption></figure><figure class="kg-card kg-image-card kg-card-hascaption"><img src="https://www.freecodecamp.org/news/content/images/2020/06/Screenshot-2020-06-15-at-23.03.32.png" class="kg-image" alt><figcaption>When the user ID is invalid</figcaption></figure><p>With this we are done with our login flow as well.</p><p>This was a lot. But now we can focus only on our chat routes.</p><h2 id="create-a-web-socket-class">Create a web socket class </h2><p>This web socket class will handle events when a user disconnects, joins a chat room, or wants to mute a chat room.</p><p>So let's create a web-socket class that will manage sockets for us. Create a new folder called <code>utils</code>. Inside that folder create a file called <code>WebSockets.js</code> and add the following content:</p><pre><code>class WebSockets {
  users = [];
  connection(client) {
    // event fired when the chat room is disconnected
    client.on("disconnect", () =&gt; {
      this.users = this.users.filter((user) =&gt; user.socketId !== client.id);
    });
    // add identity of user mapped to the socket id
    client.on("identity", (userId) =&gt; {
      this.users.push({
        socketId: client.id,
        userId: userId,
      });
    });
    // subscribe person to chat &amp; other user as well
    client.on("subscribe", (room, otherUserId = "") =&gt; {
      this.subscribeOtherUser(room, otherUserId);
      client.join(room);
    });
    // mute a chat room
    client.on("unsubscribe", (room) =&gt; {
      client.leave(room);
    });
  }

  subscribeOtherUser(room, otherUserId) {
    const userSockets = this.users.filter(
      (user) =&gt; user.userId === otherUserId
    );
    userSockets.map((userInfo) =&gt; {
      const socketConn = global.io.sockets.connected(userInfo.socketId);
      if (socketConn) {
        socketConn.join(room);
      }
    });
  }
}

export default new WebSockets();
</code></pre><p>The WebSockets class has three major things here:</p><ul><li>users array</li><li>connection method</li><li>subscribing members of a chat room to it. <code>subscribeOtherUser</code></li></ul><p>Let's break this down.</p><p>We have a class: </p><pre><code>class WebSockets {

}

export default new WebSocket();</code></pre><p>We create a class and export an instance of that class.</p><p>Inside the class we have an empty <code>users</code> array. This array will hold a list of all the active users that are online using our application.</p><p>Next we have a <code>connection</code> method, the core of this class:</p><pre><code>connection(client) {
  // event fired when the chat room is disconnected
  client.on("disconnect", () =&gt; {
    this.users = this.users.filter((user) =&gt; user.socketId !== client.id);
  });
  // add identity of user mapped to the socket id
  client.on("identity", (userId) =&gt; {
    this.users.push({
      socketId: client.id,
      userId: userId,
    });
  });
  // subscribe person to chat &amp; other user as well
  client.on("subscribe", (room, otherUserId = "") =&gt; {
    this.subscribeOtherUser(room, otherUserId);
    client.join(room);
  });
  // mute a chat room
  client.on("unsubscribe", (room) =&gt; {
    client.leave(room);
  });
}</code></pre><p>The <code>connection</code> method takes in a parameter called <code>client</code> (client here will be our server instance, I will talk more about this in a bit).</p><p>We take the param <code>client</code> and add some event to it</p><ul><li>client.on('disconnect') // when a user connection is lost this method will be called</li><li>client.on('identity') // when user logs in from the front end they will make a connection with our server by giving their identity</li><li>client.on('subscribe') // when a user joins a chat room this method is called</li><li>client.on('unsubscribe') // when a user leaves or wants to mute a chat room</li></ul><p>Let's talk about <code>disconnect</code>:</p><pre><code>client.on("disconnect", () =&gt; {
  this.users = this.users.filter((user) =&gt; user.socketId !== client.id);
});</code></pre><p>As soon as the connection is disconnected, we run a filter on users array. Where we find <code>user.id === client.id</code> we remove it from our sockets array. ( <code>client</code> here is coming from the function param.)</p><p>Let's talk about <code>identity</code>:</p><pre><code>client.on("identity", (userId) =&gt; {
  this.users.push({
    socketId: client.id,
    userId: userId,
  });
});</code></pre><p>When a user logs in through he front end application web/android/ios they will make a socket connection with our backend app and call this identity method. They'll also send their own user id.</p><p>We will take that user id and the client id (the user's own unique socket id that socket.io creates when they make a connection with our BE).</p><p>Next we have <code>unsubscribe</code>:</p><pre><code>client.on("unsubscribe", (room) =&gt; {
  client.leave(room);
});</code></pre><p>The user passes in the <code>room</code> id and we just tell <code>client.leave()</code> to remove the current user calling this method from a particular chat room.</p><p>Next we have subscribe:</p><pre><code>client.on("subscribe", (room, otherUserId = "") =&gt; {
  this.subscribeOtherUser(room, otherUserId);
  client.join(room);
});</code></pre><p>When a user joins a chat room, they will tell us about the room they want to join along with the other person who is part of that chat room.</p><p>Note: We will see later that when we initiate a chat room we get all the users associated with that room in the API response.</p><p><strong>In my opinion</strong>: Another thing we could have done here was when the user sends in the room number, we can make a DB query to see all the members of the chat room and make them join if they are online at the moment (that is, in our users list).</p><p>The <code>subscribeOtherUser</code> method is defined like this:</p><pre><code>subscribeOtherUser(room, otherUserId) {
  const userSockets = this.users.filter(
    (user) =&gt; user.userId === otherUserId
  );
  userSockets.map((userInfo) =&gt; {
    const socketConn = global.io.sockets.connected(userInfo.socketId);
    if (socketConn) {
      socketConn.join(room);
    }
  });
}</code></pre><p>We pass in  <code>room</code> and <code>otherUserId</code> as params to this function.</p><p>Using the <code>otherUserId</code> we filter on our <code>this.users</code> array and all the results that match are stored in <code>userSockets</code> array.</p><p>You might be thinking – how can one user have multiple presences in the user array? Well, think of a scenario where the same user is logged in from both their web application and mobile phone. It will create multiple socket connections for the same user.</p><p>Next we map on <code>userSockets</code>. For each item in this array we pass it into this method:  <code>const socketConn = global.io.sockets.connected(userInfo.socketId)</code> </p><p>I will talk more about this <code>global.io.sockets.connected</code> in a bit. But what this initially does is it takes in <code>userInfo.socketId</code> and if it exists in our socket connection, it will return the connection, otherwise <code>null</code>.</p><p>Next we simply see if <code>socketConn</code> is available. If so, we take that <code>socketConn</code> and make this connection join the <code>room</code> passed in the function:</p><pre><code>if (socketConn) {
	socketConn.join(room);
}</code></pre><p>And this is it for our WebSockets class.</p><p>Let's import this file in our <code>server/index.js</code> file:</p><pre><code>import socketio from "socket.io";
// mongo connection
import "./config/mongo.js";
// socket configuration
import WebSockets from "./utils/WebSockets.js";</code></pre><p>So just import <code>socket.io</code> and import <code>WebSockets</code> somewhere at the top.</p><p>Next where we are creating our server add the content below this:</p><pre><code>/** Create HTTP server. */
const server = http.createServer(app);
/** Create socket connection */
global.io = socketio.listen(server);
global.io.on('connection', WebSockets.connection)</code></pre><p>The <code>server</code> was created and we do two things:</p><ul><li>assign <code>global.io</code> to <code>socketio.listen(server)</code> (As soon as a port starts listening on the <code>server</code>, sockets starts listening for events happening on that port as well.)</li><li>then we assign <code>global.io.on('connection', WebSockets.connection)</code> method. Every time someone from the front end makes a socket connection, the <code>connection</code> method will be called which will invoke our <code>Websockets</code> class and inside that class the <code>connection</code> method.</li></ul><p><code>global.io</code> is equivalent to <code>windows</code> object in browser. But since we don't have <code>windows</code> in NodeJS we use <code>global.io</code>. Whatever we put in <code>global.io</code> is available in the entire application.</p><p>This is the same <code>global.io</code> we used in the <code>WebSockets</code> class inside the <code>subscribeOtherUser</code> method.</p><p>If you got lost here is the <a href="https://github.com/adeelibr/node-playground/tree/master/chapter-1-chat">entire source code of this chat application</a>. Also free to drop me a message with your feedback and I will try to improve the content of this tutorial.</p><h2 id="discussing-chat-room-chat-message-database-model">Discussing chat room &amp; chat message database model</h2><p>Before starting off with Chat, I think it is really important to discuss the database model on which we will create our chat application. Have a look at the below video:</p><figure class="kg-card kg-embed-card"><iframe width="480" height="270" src="https://www.youtube.com/embed/GAt-XjGvMxM?feature=oembed" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></figure><p>Now that you have a clear idea about what our chat structure will be like, let's start off by making our chat room model.</p><p>Go inside your <code>models</code> folder and create the following <code>ChatRoom.js</code>. Add the following content to it:</p><pre><code>import mongoose from "mongoose";
import { v4 as uuidv4 } from "uuid";

export const CHAT_ROOM_TYPES = {
  CONSUMER_TO_CONSUMER: "consumer-to-consumer",
  CONSUMER_TO_SUPPORT: "consumer-to-support",
};

const chatRoomSchema = new mongoose.Schema(
  {
    _id: {
      type: String,
      default: () =&gt; uuidv4().replace(/\-/g, ""),
    },
    userIds: Array,
    type: String,
    chatInitiator: String,
  },
  {
    timestamps: true,
    collection: "chatrooms",
  }
);

chatRoomSchema.statics.initiateChat = async function (
	userIds, type, chatInitiator
) {
  try {
    const availableRoom = await this.findOne({
      userIds: {
        $size: userIds.length,
        $all: [...userIds],
      },
      type,
    });
    if (availableRoom) {
      return {
        isNew: false,
        message: 'retrieving an old chat room',
        chatRoomId: availableRoom._doc._id,
        type: availableRoom._doc.type,
      };
    }

    const newRoom = await this.create({ userIds, type, chatInitiator });
    return {
      isNew: true,
      message: 'creating a new chatroom',
      chatRoomId: newRoom._doc._id,
      type: newRoom._doc.type,
    };
  } catch (error) {
    console.log('error on start chat method', error);
    throw error;
  }
}

export default mongoose.model("ChatRoom", chatRoomSchema);</code></pre><p>We have three things going on here:</p><ul><li>We have a const for <code>CHAT_ROOM_TYPES</code> which has only two types</li><li>We define our ChatRoom schema</li><li>We add a static method to initiate chat</li></ul><h2 id="chat-related-apis">Chat related APIs</h2><h3 id="initiate-a-chat-between-users-room-initiate-post-request-">Initiate a chat between users (/room/initiate [POST request])</h3><p>Let's discuss our static method defined in <code>models/ChatRoom.js</code> called <code>initiateChat</code>:</p><pre><code>chatRoomSchema.statics.initiateChat = async function (userIds, type, chatInitiator) {
  try {
    const availableRoom = await this.findOne({
      userIds: {
        $size: userIds.length,
        $all: [...userIds],
      },
      type,
    });
    if (availableRoom) {
      return {
        isNew: false,
        message: 'retrieving an old chat room',
        chatRoomId: availableRoom._doc._id,
        type: availableRoom._doc.type,
      };
    }

    const newRoom = await this.create({ userIds, type, chatInitiator });
    return {
      isNew: true,
      message: 'creating a new chatroom',
      chatRoomId: newRoom._doc._id,
      type: newRoom._doc.type,
    };
  } catch (error) {
    console.log('error on start chat method', error);
    throw error;
  }
}</code></pre><p>This function takes in three parameters:</p><ul><li>userIds (array of users)</li><li>type (type of chatroom)</li><li>chatInitiator (the user who created the chat room)</li></ul><p>Next we are doing two things here: either returning an existing chatroom document or creating a new one. </p><p>Let's break this one down:</p><pre><code>const availableRoom = await this.findOne({
  userIds: {
    $size: userIds.length,
    $all: [...userIds],
  },
  type,
});
if (availableRoom) {
  return {
    isNew: false,
    message: 'retrieving an old chat room',
    chatRoomId: availableRoom._doc._id,
    type: availableRoom._doc.type,
  };
}</code></pre><p>First using the <code>this.findOne()</code> API in mongoose, we find all the chatrooms where the following criteria is met:</p><pre><code>userIds: { $size: userIds.length, $all: [...userIds] },
type: type,</code></pre><p>You can read more on the $size operator <a href="https://docs.mongodb.com/manual/reference/operator/query/size/">here</a>, and more on the $all operator <a href="https://docs.mongodb.com/manual/reference/operator/query/all/">here</a>.</p><p>We're checking to find a chatroom document where an item exists in our chatrooms collection where</p><ol><li> the <code>userIds</code> are the same as the one we are passing to this function (irrespective of the user ids order), and </li><li>the length of the <code>userIds</code> is the same as that my <code>userIds.length</code> that we are passing through the function.</li></ol><p>Also we're checking that the chat room type should be the same.</p><p>If something like this is found, we simply return the existing chatroom.</p><p>Otherwise we create a new chat room and return it by doing this:</p><pre><code>const newRoom = await this.create({ userIds, type, chatInitiator });
return {
  isNew: true,
  message: 'creating a new chatroom',
  chatRoomId: newRoom._doc._id,
  type: newRoom._doc.type,
};</code></pre><p>Create a new room and return the response.</p><p>We also have an <code>isNew</code> key where, if it's retrieving an old chatroom, we set it to <code>false</code> otherwise <code>true</code>.</p><p>Next for your route created in <code>routes/chatRoom.js</code> called <code>post('/initiate', chatRoom.initiate)</code> go to its appropriate controller in <code>controllers/chatRoom.js</code> and add the following in the <code>initiate</code> method:</p><pre><code>initiate: async (req, res) =&gt; {
  try {
    const validation = makeValidation(types =&gt; ({
      payload: req.body,
      checks: {
        userIds: { 
          type: types.array, 
          options: { unique: true, empty: false, stringOnly: true } 
        },
        type: { type: types.enum, options: { enum: CHAT_ROOM_TYPES } },
      }
    }));
    if (!validation.success) return res.status(400).json({ ...validation });

    const { userIds, type } = req.body;
    const { userId: chatInitiator } = req;
    const allUserIds = [...userIds, chatInitiator];
    const chatRoom = await ChatRoomModel.initiateChat(allUserIds, type, chatInitiator);
    return res.status(200).json({ success: true, chatRoom });
  } catch (error) {
    return res.status(500).json({ success: false, error: error })
  }
},</code></pre><p>We are using the <code><a href="https://www.npmjs.com/package/@withvoid/make-validation">make-validation</a></code> library here to validate the user's request. For the initiate API, we expect the user to send an array of <code>users</code> and also define the type of the <code>chat-room</code> that is being created.</p><p>Once the validation passes, then:</p><pre><code>const { userIds, type } = req.body;
const { userId: chatInitiator } = req;
const allUserIds = [...userIds, chatInitiator];
const chatRoom = await ChatRoomModel.initiateChat(allUserIds, type, chatInitiator);
return res.status(200).json({ success: true, chatRoom });</code></pre><p>One thing to notice here is <code>userIds, type</code> is coming from <code>req.body</code> while <code>userId</code> that is being aliased as <code>chatInitiatorId</code> is coming from <code>req</code> thanks to our <code>decode</code> middleware.</p><p>If you remember, we attached <code>app.use("/room", decode, chatRoomRouter);</code> in our <code>server/index.js</code> file. This means this route <code>/room/initiate</code> is authenticated. So <code>const { userId: chatInitiator } = req;</code> is the id of the current user logged in.</p><p>We simply call our <code>initiateChat</code> method from <code>ChatRoomModel</code> and pass it <code>allUserIds, type, chatInitiator</code>. Whatever result comes we simply pass it to the user.</p><p>Let's run this and see if it works (here is a video of me doing it):</p><figure class="kg-card kg-embed-card"><iframe width="459" height="344" src="https://www.youtube.com/embed/vWzmTrNoNJs?feature=oembed" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></figure><h3 id="create-a-message-in-chat-room-roomid-message-post-request-">Create a message in chat room (/:roomId/message) [POST request]</h3><p>Let's create a message for the chat room we just created with <code>pikachu</code>.</p><p>But before we create a message we need to create a model for our <code>chatmessages</code>. So let's do that first. In your <code>models</code> folder create a new file called <code>ChatMessage.js</code> and add the following content to it:</p><pre><code>import mongoose from "mongoose";
import { v4 as uuidv4 } from "uuid";

const MESSAGE_TYPES = {
  TYPE_TEXT: "text",
};

const readByRecipientSchema = new mongoose.Schema(
  {
    _id: false,
    readByUserId: String,
    readAt: {
      type: Date,
      default: Date.now(),
    },
  },
  {
    timestamps: false,
  }
);

const chatMessageSchema = new mongoose.Schema(
  {
    _id: {
      type: String,
      default: () =&gt; uuidv4().replace(/\-/g, ""),
    },
    chatRoomId: String,
    message: mongoose.Schema.Types.Mixed,
    type: {
      type: String,
      default: () =&gt; MESSAGE_TYPES.TYPE_TEXT,
    },
    postedByUser: String,
    readByRecipients: [readByRecipientSchema],
  },
  {
    timestamps: true,
    collection: "chatmessages",
  }
);

chatMessageSchema.statics.createPostInChatRoom = async function (chatRoomId, message, postedByUser) {
  try {
    const post = await this.create({
      chatRoomId,
      message,
      postedByUser,
      readByRecipients: { readByUserId: postedByUser }
    });
    const aggregate = await this.aggregate([
      // get post where _id = post._id
      { $match: { _id: post._id } },
      // do a join on another table called users, and 
      // get me a user whose _id = postedByUser
      {
        $lookup: {
          from: 'users',
          localField: 'postedByUser',
          foreignField: '_id',
          as: 'postedByUser',
        }
      },
      { $unwind: '$postedByUser' },
      // do a join on another table called chatrooms, and 
      // get me a chatroom whose _id = chatRoomId
      {
        $lookup: {
          from: 'chatrooms',
          localField: 'chatRoomId',
          foreignField: '_id',
          as: 'chatRoomInfo',
        }
      },
      { $unwind: '$chatRoomInfo' },
      { $unwind: '$chatRoomInfo.userIds' },
      // do a join on another table called users, and 
      // get me a user whose _id = userIds
      {
        $lookup: {
          from: 'users',
          localField: 'chatRoomInfo.userIds',
          foreignField: '_id',
          as: 'chatRoomInfo.userProfile',
        }
      },
      { $unwind: '$chatRoomInfo.userProfile' },
      // group data
      {
        $group: {
          _id: '$chatRoomInfo._id',
          postId: { $last: '$_id' },
          chatRoomId: { $last: '$chatRoomInfo._id' },
          message: { $last: '$message' },
          type: { $last: '$type' },
          postedByUser: { $last: '$postedByUser' },
          readByRecipients: { $last: '$readByRecipients' },
          chatRoomInfo: { $addToSet: '$chatRoomInfo.userProfile' },
          createdAt: { $last: '$createdAt' },
          updatedAt: { $last: '$updatedAt' },
        }
      }
    ]);
    return aggregate[0];
  } catch (error) {
    throw error;
  }
}

export default mongoose.model("ChatMessage", chatMessageSchema);</code></pre><p>There are a couple of things happening here:</p><ul><li>We have a <code>MESSAGE_TYPES</code> object which has only one type called <code>text</code></li><li>We are defining our schema for <code>chatmessage</code> and <code>readByRecipient</code></li><li>Then we are writing our static method for <code>createPostInChatRoom</code></li></ul><p>I know this is a lot of content, but just bear with me. Let's just write the controller for the route that creates this message.</p><p>For the route defined in our <code>routes/chatRoom.js</code> API called <code>.post('/:roomId/message', chatRoom.postMessage)</code> let's go to its controller in <code>controllers/chatRoom.js</code> and define it:</p><pre><code>postMessage: async (req, res) =&gt; {
  try {
    const { roomId } = req.params;
    const validation = makeValidation(types =&gt; ({
      payload: req.body,
      checks: {
        messageText: { type: types.string },
      }
    }));
    if (!validation.success) return res.status(400).json({ ...validation });

    const messagePayload = {
      messageText: req.body.messageText,
    };
    const currentLoggedUser = req.userId;
    const post = await ChatMessageModel.createPostInChatRoom(roomId, messagePayload, currentLoggedUser);
    global.io.sockets.in(roomId).emit('new message', { message: post });
    return res.status(200).json({ success: true, post });
  } catch (error) {
    return res.status(500).json({ success: false, error: error })
  }
},</code></pre><p>Cool, let's discuss what we are doing here:</p><figure class="kg-card kg-embed-card"><iframe width="459" height="344" src="https://www.youtube.com/embed/z1C0Sl2wmJU?feature=oembed" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></figure><p>Operators discussed in this video are:</p><ul><li><a href="https://docs.mongodb.com/manual/reference/operator/aggregation/match/">$match</a></li><li><a href="https://docs.mongodb.com/manual/reference/operator/aggregation/last/">$last</a></li><li><a href="https://docs.mongodb.com/manual/reference/operator/update/addToSet/">$addToSet</a></li><li><a href="https://docs.mongodb.com/manual/reference/operator/aggregation/lookup/">$lookup</a></li><li><a href="https://docs.mongodb.com/manual/reference/operator/aggregation/unwind/">$unwind</a></li><li><a href="https://docs.mongodb.com/manual/reference/operator/aggregation/group/">$group</a></li></ul><h3 id="see-conversation-for-a-chat-room-by-it-s-id-get-request-">See conversation for a chat room by it's id [Get request]</h3><p>Now that we have</p><ul><li>Created a chat room</li><li>Are able to add messages in that chat room</li></ul><p>Let's see the entire conversation for that chat as well (with pagination).</p><p>For your route <code>.get('/:roomId', chatRoom.getConversationByRoomId)</code> in <code>routes/chatRoom.js</code> open its controller in the file <code>controllers/chatRoom.js</code> and add the following content to the chat room:</p><pre><code>getConversationByRoomId: async (req, res) =&gt; {
  try {
    const { roomId } = req.params;
    const room = await ChatRoomModel.getChatRoomByRoomId(roomId)
    if (!room) {
      return res.status(400).json({
        success: false,
        message: 'No room exists for this id',
      })
    }
    const users = await UserModel.getUserByIds(room.userIds);
    const options = {
      page: parseInt(req.query.page) || 0,
      limit: parseInt(req.query.limit) || 10,
    };
    const conversation = await ChatMessageModel.getConversationByRoomId(roomId, options);
    return res.status(200).json({
      success: true,
      conversation,
      users,
    });
  } catch (error) {
    return res.status(500).json({ success: false, error });
  }
},</code></pre><p>Next let's create a new static method in our <code>ChatRoomModel</code> file called <code>getChatRoomByRoomId</code> in <code>models/ChatRoom.js</code>:</p><!--kg-card-begin: markdown--><pre><code>chatRoomSchema.statics.getChatRoomByRoomId = async function (roomId) {
  try {
    const room = await this.findOne({ _id: roomId });
    return room;
  } catch (error) {
    throw error;
  }
}
</code></pre>
<!--kg-card-end: markdown--><p>Very straightforward – we are getting the room by roomId here.</p><p>Next in our <code>UserModel</code>, create a static method called <code>getUserByIds</code> in the file <code>models/User.js</code>:</p><pre><code>userSchema.statics.getUserByIds = async function (ids) {
  try {
    const users = await this.find({ _id: { $in: ids } });
    return users;
  } catch (error) {
    throw error;
  }
}</code></pre><p>The operator used here is <a href="https://docs.mongodb.com/manual/reference/operator/query/in/">$in</a> – I'll talk about this in a bit.</p><p>And then at last, go to your <code>ChatMessage</code> model in <code>models/ChatMessage.js</code> and write a new static method called <code>getConversationByRoomId</code>:</p><pre><code>chatMessageSchema.statics.getConversationByRoomId = async function (chatRoomId, options = {}) {
  try {
    return this.aggregate([
      { $match: { chatRoomId } },
      { $sort: { createdAt: -1 } },
      // do a join on another table called users, and 
      // get me a user whose _id = postedByUser
      {
        $lookup: {
          from: 'users',
          localField: 'postedByUser',
          foreignField: '_id',
          as: 'postedByUser',
        }
      },
      { $unwind: "$postedByUser" },
      // apply pagination
      { $skip: options.page * options.limit },
      { $limit: options.limit },
      { $sort: { createdAt: 1 } },
    ]);
  } catch (error) {
    throw error;
  }
}</code></pre><p>Let's discuss all that we have done so far:</p><figure class="kg-card kg-embed-card"><iframe width="459" height="344" src="https://www.youtube.com/embed/cnwOMrVMv0c?feature=oembed" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></figure><p><strong><a href="https://github.com/adeelibr/node-playground/tree/master/chapter-1-chat">All the source code is available here</a>.</strong></p><h3 id="mark-an-entire-conversation-as-read-feature-similar-to-whatsapp-">Mark an entire conversation as read (feature similar to WhatsApp)</h3><p>Once the other person is logged in and they view a conversation for a room id, we need to mark that conversation as read from their side.</p><p>To do this, in your <code>routes/chatRoom.js</code> for the route </p><pre><code>put('/:roomId/mark-read', chatRoom.markConversationReadByRoomId)</code></pre><p>go to its appropriate controller in <code>controllers/chatRoom.js</code> and add the following content in the <code>markConversationReadByRoomId</code> controller.</p><pre><code>markConversationReadByRoomId: async (req, res) =&gt; {
  try {
    const { roomId } = req.params;
    const room = await ChatRoomModel.getChatRoomByRoomId(roomId)
    if (!room) {
      return res.status(400).json({
        success: false,
        message: 'No room exists for this id',
      })
    }

    const currentLoggedUser = req.userId;
    const result = await ChatMessageModel.markMessageRead(roomId, currentLoggedUser);
    return res.status(200).json({ success: true, data: result });
  } catch (error) {
    console.log(error);
    return res.status(500).json({ success: false, error });
  }
},</code></pre><p>All we are doing here is first checking if the room exists or not. If it does, we proceed further. We take in the <code>req.user.id</code> as <code>currentLoggedUser</code> and pass it to the following function:</p><pre><code>ChatMessageModel.markMessageRead(roomId, currentLoggedUser);</code></pre><p>Which in our <code>ChatMessage</code> model is defined like this:</p><pre><code>chatMessageSchema.statics.markMessageRead = async function (chatRoomId, currentUserOnlineId) {
  try {
    return this.updateMany(
      {
        chatRoomId,
        'readByRecipients.readByUserId': { $ne: currentUserOnlineId }
      },
      {
        $addToSet: {
          readByRecipients: { readByUserId: currentUserOnlineId }
        }
      },
      {
        multi: true
      }
    );
  } catch (error) {
    throw error;
  }
}</code></pre><p>A possible use case is that the user might not have read the last 15 messages once they open up a specific room conversation. They should all be marked as read. So we're using the <code>this.updateMany</code> function by mongoose.</p><p>The query itself is defined in 2 steps:</p><ul><li>Find</li><li>Update</li></ul><p>And there can be multiple statements be updated.</p><p>To find a section, do this:</p><pre><code>{
  chatRoomId,
  'readByRecipients.readByUserId': { $ne: currentUserOnlineId }
},</code></pre><p>This says I want to find all the message posts in the <code>chatmessages</code> collection where <code>chatRoomId</code> matches and <code>readByRecipients</code> array does not. The <code>userId</code> that I am passing to this function is <code>currentUserOnlineId</code>.</p><p>Once it has all those documents where the criteria matches, it's then time to update them:</p><pre><code>{
  $addToSet: {
    readByRecipients: { readByUserId: currentUserOnlineId }
  }
},</code></pre><p><code>$addToSet</code> will just push a new entry to the <code>readByRecipients</code> array. This is like <code>Array.push</code> but for mongo. </p><p>Next we want to tell <code>mongoose</code> to not just update the first record it finds, but also to update all the records where the condition matches. So doing this:</p><pre><code>{
  multi: true
}</code></pre><p>And that is all – we return the data as is.</p><p>Let's run this API.</p><p>Start up the server:</p><pre><code>npm start;</code></pre><p>Open your postman and create a new <code>PUT</code> request to test this route <code>ocalhost:3000/room/&lt;room=id-here&gt;/mark-read</code>:</p><figure class="kg-card kg-image-card"><img src="https://www.freecodecamp.org/news/content/images/2020/06/Screenshot-2020-06-16-at-23.20.53.png" class="kg-image" alt></figure><h3 id="bonus-section">Bonus Section</h3><ul><li>How to delete a chat room and all its related messages</li><li>How to delete a message by its message id</li></ul><figure class="kg-card kg-embed-card"><iframe width="459" height="344" src="https://www.youtube.com/embed/GHhOIg5ZDa4?feature=oembed" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></figure><p>And we are done! Wow that was a lot of learning today.</p><p>You can find the source code of this tutorial <a href="https://github.com/adeelibr/node-playground/tree/master/chapter-1-chat">here</a>.</p><p>Reach out to me on twitter with your feedback – I would love to hear if you have any suggestions for improvements: <a href="https://twitter.com/adeelibr">twitter.com/adeelibr</a></p><p>If you liked to this article, please do give the <a href="https://github.com/adeelibr/node-playground/tree/master/chapter-1-chat">github repository</a> a star and subscribe to my <a href="https://www.youtube.com/channel/UCGHFI8lm4QzUzFH5nnzqkjA">youtube channel</a>.</p>
                </div>
                <hr />

                <div class="post-full-author-header">
                    
<section class="author-card">
    <img class="author-profile-image" src="/news/content/images/size/w100/2019/11/16651811.jpeg" alt="Adeel Imran" />
    <section class="author-card-content">
        <h4 class="author-card-name"><a href="/news/author/adeel/">Adeel Imran</a></h4>
        <p>Developer &amp; maybe a conference speaker one day.
</p>
    </section>
</section>


                </div>
                <hr />

                <p class="social-row">

    If you read this far, tweet to the author to show them you care. <a id='tweet-btn' class='cta-button'>Tweet a thanks</a>
</p>

                
<div class='learn-cta-row'>
    <p>
        Learn to code for free. freeCodeCamp&#x27;s open source curriculum has helped more than 40,000 people get jobs as developers. <a class="cta-button" id="learn-to-code-cta" rel="noopener noreferrer" target="_blank">Get started</a>
    </p>
</div>

                  <script>
    // Conditionally show comments section based on publication language setting
    const showCommentsList = ['zh-cn'];

    if (showCommentsList.includes(`en`)) {
      const hostname = window.location.hostname;
      const discourseEmbedMap = {
        'www.freecodecamp.org': {
          file: 'https://forum.freecodecamp.org/srv/status',
          discourseUrl: 'https://forum.freecodecamp.org/'
        },
        'chinese.freecodecamp.org': {
          file: 'https://chinese.freecodecamp.org/forum/srv/status',
          discourseUrl: 'https://chinese.freecodecamp.org/forum/',
        },
        'dev': {
          file: 'https://forum.freecodecamp.dev/srv/status',
          discourseUrl: 'https://forum.freecodecamp.dev/'
        },
      };
      const discourseEmbedInfo = discourseEmbedMap[hostname] ? discourseEmbedMap[hostname] : discourseEmbedMap['dev'];
      const { file, discourseUrl } = discourseEmbedInfo;

      function loadDiscourseComments() {
        var xhr = new XMLHttpRequest();
        var randomNum = Math.round(Math.random() * 10000);
        xhr.open('HEAD', file + '?rand=' + randomNum, true);
        xhr.send();
        xhr.addEventListener('readystatechange', processRequest, false);
        function processRequest(e) {
          if (xhr.readyState == 4) {
            if (xhr.status >= 200 && xhr.status < 304) {
              document.getElementById('discourse-comments').innerHTML = '';
              DiscourseEmbed = {
                discourseUrl,
                discourseEmbedUrl: 'https://www.freecodecamp.org/news/create-a-professional-node-express/'
              };
              var d = document.createElement('script');
              d.type = 'text/javascript';
              d.async = true;
              d.src = discourseUrl + 'javascripts/embed.js';
              (document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0]).appendChild(d);
            } else {
              document.getElementById('discourse-comments').innerHTML =
                '<div style="text-align: center;">Sorry, we could not load the comments. Please try again after some time.</div>';
            }
          }
        }
      }

      if (window && window.addEventListener) {
        // Create comments section
        const commentsDivHtml = `
          <div id='discourse-comments'>
            <button id='trigger-load-comments'>Show comments</button>
          </div>
        `;
        const fullContentSection = document.getElementsByClassName('post-full-content')[0];
        fullContentSection.insertAdjacentHTML('beforeend', commentsDivHtml);

        window.addEventListener('load', function () {
          document.getElementById('trigger-load-comments').onclick = loadDiscourseComments;
        });
      }
    }
  </script>
            </section>

        </article>
    </div>
</main>




        <footer class="site-footer">
    <div class="footer-container">
        <div class="footer-top">
            <div class="footer-desc-col">
                <p>
                    freeCodeCamp is a donor-supported tax-exempt 501(c)(3) nonprofit organization (United States Federal Tax Identification Number: 82-0779546)
                </p>
                <p>
                    Our mission: to help people learn to code for free. We accomplish this by creating thousands of videos, articles, and interactive coding lessons - all freely available to the public. We also have thousands of freeCodeCamp study groups around the world.
                </p>
                <p>
                    Donations to freeCodeCamp go toward our education initiatives, and help pay for servers, services, and staff.
                </p>
                <p class="footer-donation">
                    You can <a id='footer-donation' class='inline' rel='noopener noreferrer' target='_blank'>make a tax-deductible donation here</a>.
                </p>
            </div>
            <div class="trending-guides">
                <div class="col-header">Trending Guides</div>
                <div class="trending-guides-row">
                    <div class="footer-col footer-col-1">
                        <a id="article0" rel="noopener noreferrer" target="_blank"></a>
                        <a id="article1" rel="noopener noreferrer" target="_blank"></a>
                        <a id="article2" rel="noopener noreferrer" target="_blank"></a>
                        <a id="article3" rel="noopener noreferrer" target="_blank"></a>
                        <a id="article4" rel="noopener noreferrer" target="_blank"></a>
                        <a id="article5" rel="noopener noreferrer" target="_blank"></a>
                        <a id="article6" rel="noopener noreferrer" target="_blank"></a>
                        <a id="article7" rel="noopener noreferrer" target="_blank"></a>
                        <a id="article8" rel="noopener noreferrer" target="_blank"></a>
                        <a id="article9" rel="noopener noreferrer" target="_blank"></a>
                    </div>
                    <div class="footer-col footer-col-2">
                        <a id="article10" rel="noopener noreferrer" target="_blank"></a>
                        <a id="article11" rel="noopener noreferrer" target="_blank"></a>
                        <a id="article12" rel="noopener noreferrer" target="_blank"></a>
                        <a id="article13" rel="noopener noreferrer" target="_blank"></a>
                        <a id="article14" rel="noopener noreferrer" target="_blank"></a>
                        <a id="article15" rel="noopener noreferrer" target="_blank"></a>
                        <a id="article16" rel="noopener noreferrer" target="_blank"></a>
                        <a id="article17" rel="noopener noreferrer" target="_blank"></a>
                        <a id="article18" rel="noopener noreferrer" target="_blank"></a>
                        <a id="article19" rel="noopener noreferrer" target="_blank"></a>
                    </div>
                    <div class="footer-col footer-col-3">
                        <div class="footer-left">
                            <a id="article20" rel="noopener noreferrer" target="_blank"></a>
                            <a id="article21" rel="noopener noreferrer" target="_blank"></a>
                            <a id="article22" rel="noopener noreferrer" target="_blank"></a>
                            <a id="article23" rel="noopener noreferrer" target="_blank"></a>
                            <a id="article24" rel="noopener noreferrer" target="_blank"></a>
                        </div>

                        <div class="footer-right">
                            <a id="article25" rel="noopener noreferrer" target="_blank"></a>
                            <a id="article26" rel="noopener noreferrer" target="_blank"></a>
                            <a id="article27" rel="noopener noreferrer" target="_blank"></a>
                            <a id="article28" rel="noopener noreferrer" target="_blank"></a>
                            <a id="article29" rel="noopener noreferrer" target="_blank"></a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class='footer-bottom'>
            <div class="col-header">Our Nonprofit</div>
            <div class="footer-divider"></div>
            <div class="our-nonprofit">
                <a id="about" rel="noopener noreferrer" target="_blank">About</a>
                <a id="alumni" rel="noopener noreferrer" target="_blank">Alumni Network</a>
                <a id="open-source" rel="noopener noreferrer" target="_blank">Open Source</a>
                <a id="shop" rel="noopener noreferrer" target="_blank">Shop</a>
                <a id="support" rel="noopener noreferrer" target="_blank">Support</a>
                <a id="sponsors" rel="noopener noreferrer" target="_blank">Sponsors</a>
                <a id="honesty" rel="noopener noreferrer" target="_blank">Academic Honesty</a>
                <a id="coc" rel="noopener noreferrer" target="_blank">Code of Conduct</a>
                <a id="privacy" rel="noopener noreferrer" target="_blank">Privacy Policy</a>
                <a id="tos" rel="noopener noreferrer" target="_blank">Terms of Service</a>
                <a id="copyright" rel="noopener noreferrer" target="_blank">Copyright Policy</a>
            </div>
        </div>
    </div>
</footer>


    </div>

    <script>
        var images = document.querySelectorAll('.kg-gallery-image img');
        images.forEach(function (image) {
            var container = image.closest('.kg-gallery-image');
            var width = image.attributes.width.value;
            var height = image.attributes.height.value;
            var ratio = width / height;
            container.style.flex = ratio + ' 1 0%';
        })
    </script>

    <script src="https://code.jquery.com/jquery-3.2.1.min.js"
        integrity="sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=" crossorigin="anonymous">
        </script>
    <script type="text/javascript" src="/news/assets/built/jquery.fitvids.js?v=17fe0e02db"></script>

    <script type="text/javascript" src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-unescaped-markup.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-markup-templating.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-bash.min.js"></script>
    <script type="text/javascript" src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-c.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-clojure.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-cpp.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-csharp.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-css.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-docker.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-elixir.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-erlang.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-git.min.js"></script>
    <script type="text/javascript" src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-go.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-graphql.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-haskell.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-java.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-javascript.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-json.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-jsx.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-kotlin.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-lua.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-markup.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-php.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-python.min.js"></script>
    <script type="text/javascript" src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-r.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-ruby.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-rust.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-scala.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-sql.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-swift.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-typescript.min.js"></script>
    <script type="text/javascript"
        src="https://cdn.freecodecamp.org/news-assets/prism-1-16-0/prism-yaml.min.js"></script>

    <script>
    // Conditionally remove social-row based on the publication language setting
    const hideSocialRowList = ['zh-cn'];
    const socialRow = document.getElementsByClassName('social-row')[0];

    if (hideSocialRowList.includes(`en`)) socialRow.remove();
    else {
        const title = `How%20to%20Create%20a%20Professional%20Chat%20API%20Solution%20with%20Sockets%20in%20NodeJS%20%5BBeginner%20level%5D`.replace(/'/g, '%27');
        const twitter = `@adeelibr`;
        const url = window.location;
        const thanks = `Thank%20you%20%40adeelibr%20for%20writing%20this%20helpful%20article.` +
            `%0A%0A${title}%0A%0A${url}`;
        const button = document.getElementById('tweet-btn');
        button.addEventListener('click', () => {
            if (twitter) {
                window.open(`https://twitter.com/intent/tweet?text=${thanks}`, `share-twitter`, `width=550, height=235`);
                return false;
            }
            else {
                window.open(`https://twitter.com/intent/tweet?text=${title}%0A%0A${url}`, `share-twitter`, `width=550, height=235`);
                return false;
            }
        });
    }
</script>

<script>
    const learnToCodeCtaAnchorEl = document.getElementById('learn-to-code-cta');

    learnToCodeCtaAnchorEl.href = main['learn-to-code-cta-url'];
</script>

<script>
    $(document).ready(function () {
        // Start fitVids
        var $postContent = $(".post-full-content");
        $postContent.fitVids();
        // End fitVids
    });
</script>

<script>
    const navForumAnchorEl = document.getElementById('nav-forum');
    const navDonateAnchorEl = document.getElementById('nav-donate');

    navForumAnchorEl.href = main['forum-url'];
    navDonateAnchorEl.href = main['donate-url'];
</script>

<script>
    const bannerAnchorEl = document.getElementById('banner');

    bannerAnchorEl.href = main['banner-url'];
</script>

<script>
    const { trending, ...otherUrls } = footer;
    const footerDonationAnchorEl = document.getElementById('footer-donation');

    Object.keys(trending).forEach(key => {
        const anchorId = key.replace(/link|title/, '');
        const trendingAnchorEl = document.getElementById(anchorId);

        if (key.includes('link')) {
            trendingAnchorEl.href = trending[key]
        } else if (key.includes('title')) {
            trendingAnchorEl.textContent = trending[key];
        }
    });

    Object.keys(otherUrls).forEach(key => {
        const footerAnchorEl = document.getElementById(key);

        footerAnchorEl.href = otherUrls[key];
    });

    footerDonationAnchorEl.href = main['donate-url'];
</script>


    <!-- Google Tag Manager (noscript) -->
<noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-5D6RKKP"
height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript>
<!-- End Google Tag Manager (noscript) -->

</body>

</html>
