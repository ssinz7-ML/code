                                      1 ;--------------------------------------------------------
                                      2 ; File Created by SDCC : free open source ANSI-C Compiler
                                      3 ; Version 4.0.0 #11528 (Linux)
                                      4 ;--------------------------------------------------------
                                      5 	.module test
                                      6 	.optsdcc -mmcs51 --model-small
                                      7 	
                                      8 ;--------------------------------------------------------
                                      9 ; Public variables in this module
                                     10 ;--------------------------------------------------------
                                     11 	.globl _main
                                     12 	.globl _Delay
                                     13 	.globl _CY
                                     14 	.globl _AC
                                     15 	.globl _F0
                                     16 	.globl _RS1
                                     17 	.globl _RS0
                                     18 	.globl _OV
                                     19 	.globl _F1
                                     20 	.globl _P
                                     21 	.globl _PS
                                     22 	.globl _PT1
                                     23 	.globl _PX1
                                     24 	.globl _PT0
                                     25 	.globl _PX0
                                     26 	.globl _RD
                                     27 	.globl _WR
                                     28 	.globl _T1
                                     29 	.globl _T0
                                     30 	.globl _INT1
                                     31 	.globl _INT0
                                     32 	.globl _TXD
                                     33 	.globl _RXD
                                     34 	.globl _P3_7
                                     35 	.globl _P3_6
                                     36 	.globl _P3_5
                                     37 	.globl _P3_4
                                     38 	.globl _P3_3
                                     39 	.globl _P3_2
                                     40 	.globl _P3_1
                                     41 	.globl _P3_0
                                     42 	.globl _EA
                                     43 	.globl _ES
                                     44 	.globl _ET1
                                     45 	.globl _EX1
                                     46 	.globl _ET0
                                     47 	.globl _EX0
                                     48 	.globl _P2_7
                                     49 	.globl _P2_6
                                     50 	.globl _P2_5
                                     51 	.globl _P2_4
                                     52 	.globl _P2_3
                                     53 	.globl _P2_2
                                     54 	.globl _P2_1
                                     55 	.globl _P2_0
                                     56 	.globl _SM0
                                     57 	.globl _SM1
                                     58 	.globl _SM2
                                     59 	.globl _REN
                                     60 	.globl _TB8
                                     61 	.globl _RB8
                                     62 	.globl _TI
                                     63 	.globl _RI
                                     64 	.globl _P1_7
                                     65 	.globl _P1_6
                                     66 	.globl _P1_5
                                     67 	.globl _P1_4
                                     68 	.globl _P1_3
                                     69 	.globl _P1_2
                                     70 	.globl _P1_1
                                     71 	.globl _P1_0
                                     72 	.globl _TF1
                                     73 	.globl _TR1
                                     74 	.globl _TF0
                                     75 	.globl _TR0
                                     76 	.globl _IE1
                                     77 	.globl _IT1
                                     78 	.globl _IE0
                                     79 	.globl _IT0
                                     80 	.globl _P0_7
                                     81 	.globl _P0_6
                                     82 	.globl _P0_5
                                     83 	.globl _P0_4
                                     84 	.globl _P0_3
                                     85 	.globl _P0_2
                                     86 	.globl _P0_1
                                     87 	.globl _P0_0
                                     88 	.globl _B
                                     89 	.globl _ACC
                                     90 	.globl _PSW
                                     91 	.globl _IP
                                     92 	.globl _P3
                                     93 	.globl _IE
                                     94 	.globl _P2
                                     95 	.globl _SBUF
                                     96 	.globl _SCON
                                     97 	.globl _P1
                                     98 	.globl _TH1
                                     99 	.globl _TH0
                                    100 	.globl _TL1
                                    101 	.globl _TL0
                                    102 	.globl _TMOD
                                    103 	.globl _TCON
                                    104 	.globl _PCON
                                    105 	.globl _DPH
                                    106 	.globl _DPL
                                    107 	.globl _SP
                                    108 	.globl _P0
                                    109 	.globl _tab
                                    110 ;--------------------------------------------------------
                                    111 ; special function registers
                                    112 ;--------------------------------------------------------
                                    113 	.area RSEG    (ABS,DATA)
      000000                        114 	.org 0x0000
                           000080   115 _P0	=	0x0080
                           000081   116 _SP	=	0x0081
                           000082   117 _DPL	=	0x0082
                           000083   118 _DPH	=	0x0083
                           000087   119 _PCON	=	0x0087
                           000088   120 _TCON	=	0x0088
                           000089   121 _TMOD	=	0x0089
                           00008A   122 _TL0	=	0x008a
                           00008B   123 _TL1	=	0x008b
                           00008C   124 _TH0	=	0x008c
                           00008D   125 _TH1	=	0x008d
                           000090   126 _P1	=	0x0090
                           000098   127 _SCON	=	0x0098
                           000099   128 _SBUF	=	0x0099
                           0000A0   129 _P2	=	0x00a0
                           0000A8   130 _IE	=	0x00a8
                           0000B0   131 _P3	=	0x00b0
                           0000B8   132 _IP	=	0x00b8
                           0000D0   133 _PSW	=	0x00d0
                           0000E0   134 _ACC	=	0x00e0
                           0000F0   135 _B	=	0x00f0
                                    136 ;--------------------------------------------------------
                                    137 ; special function bits
                                    138 ;--------------------------------------------------------
                                    139 	.area RSEG    (ABS,DATA)
      000000                        140 	.org 0x0000
                           000080   141 _P0_0	=	0x0080
                           000081   142 _P0_1	=	0x0081
                           000082   143 _P0_2	=	0x0082
                           000083   144 _P0_3	=	0x0083
                           000084   145 _P0_4	=	0x0084
                           000085   146 _P0_5	=	0x0085
                           000086   147 _P0_6	=	0x0086
                           000087   148 _P0_7	=	0x0087
                           000088   149 _IT0	=	0x0088
                           000089   150 _IE0	=	0x0089
                           00008A   151 _IT1	=	0x008a
                           00008B   152 _IE1	=	0x008b
                           00008C   153 _TR0	=	0x008c
                           00008D   154 _TF0	=	0x008d
                           00008E   155 _TR1	=	0x008e
                           00008F   156 _TF1	=	0x008f
                           000090   157 _P1_0	=	0x0090
                           000091   158 _P1_1	=	0x0091
                           000092   159 _P1_2	=	0x0092
                           000093   160 _P1_3	=	0x0093
                           000094   161 _P1_4	=	0x0094
                           000095   162 _P1_5	=	0x0095
                           000096   163 _P1_6	=	0x0096
                           000097   164 _P1_7	=	0x0097
                           000098   165 _RI	=	0x0098
                           000099   166 _TI	=	0x0099
                           00009A   167 _RB8	=	0x009a
                           00009B   168 _TB8	=	0x009b
                           00009C   169 _REN	=	0x009c
                           00009D   170 _SM2	=	0x009d
                           00009E   171 _SM1	=	0x009e
                           00009F   172 _SM0	=	0x009f
                           0000A0   173 _P2_0	=	0x00a0
                           0000A1   174 _P2_1	=	0x00a1
                           0000A2   175 _P2_2	=	0x00a2
                           0000A3   176 _P2_3	=	0x00a3
                           0000A4   177 _P2_4	=	0x00a4
                           0000A5   178 _P2_5	=	0x00a5
                           0000A6   179 _P2_6	=	0x00a6
                           0000A7   180 _P2_7	=	0x00a7
                           0000A8   181 _EX0	=	0x00a8
                           0000A9   182 _ET0	=	0x00a9
                           0000AA   183 _EX1	=	0x00aa
                           0000AB   184 _ET1	=	0x00ab
                           0000AC   185 _ES	=	0x00ac
                           0000AF   186 _EA	=	0x00af
                           0000B0   187 _P3_0	=	0x00b0
                           0000B1   188 _P3_1	=	0x00b1
                           0000B2   189 _P3_2	=	0x00b2
                           0000B3   190 _P3_3	=	0x00b3
                           0000B4   191 _P3_4	=	0x00b4
                           0000B5   192 _P3_5	=	0x00b5
                           0000B6   193 _P3_6	=	0x00b6
                           0000B7   194 _P3_7	=	0x00b7
                           0000B0   195 _RXD	=	0x00b0
                           0000B1   196 _TXD	=	0x00b1
                           0000B2   197 _INT0	=	0x00b2
                           0000B3   198 _INT1	=	0x00b3
                           0000B4   199 _T0	=	0x00b4
                           0000B5   200 _T1	=	0x00b5
                           0000B6   201 _WR	=	0x00b6
                           0000B7   202 _RD	=	0x00b7
                           0000B8   203 _PX0	=	0x00b8
                           0000B9   204 _PT0	=	0x00b9
                           0000BA   205 _PX1	=	0x00ba
                           0000BB   206 _PT1	=	0x00bb
                           0000BC   207 _PS	=	0x00bc
                           0000D0   208 _P	=	0x00d0
                           0000D1   209 _F1	=	0x00d1
                           0000D2   210 _OV	=	0x00d2
                           0000D3   211 _RS0	=	0x00d3
                           0000D4   212 _RS1	=	0x00d4
                           0000D5   213 _F0	=	0x00d5
                           0000D6   214 _AC	=	0x00d6
                           0000D7   215 _CY	=	0x00d7
                                    216 ;--------------------------------------------------------
                                    217 ; overlayable register banks
                                    218 ;--------------------------------------------------------
                                    219 	.area REG_BANK_0	(REL,OVR,DATA)
      000000                        220 	.ds 8
                                    221 ;--------------------------------------------------------
                                    222 ; internal ram data
                                    223 ;--------------------------------------------------------
                                    224 	.area DSEG    (DATA)
      000008                        225 _tab::
      000008                        226 	.ds 8
                                    227 ;--------------------------------------------------------
                                    228 ; overlayable items in internal ram 
                                    229 ;--------------------------------------------------------
                                    230 	.area	OSEG    (OVR,DATA)
                                    231 ;--------------------------------------------------------
                                    232 ; Stack segment in internal ram 
                                    233 ;--------------------------------------------------------
                                    234 	.area	SSEG
      000010                        235 __start__stack:
      000010                        236 	.ds	1
                                    237 
                                    238 ;--------------------------------------------------------
                                    239 ; indirectly addressable internal ram data
                                    240 ;--------------------------------------------------------
                                    241 	.area ISEG    (DATA)
                                    242 ;--------------------------------------------------------
                                    243 ; absolute internal ram data
                                    244 ;--------------------------------------------------------
                                    245 	.area IABS    (ABS,DATA)
                                    246 	.area IABS    (ABS,DATA)
                                    247 ;--------------------------------------------------------
                                    248 ; bit data
                                    249 ;--------------------------------------------------------
                                    250 	.area BSEG    (BIT)
                                    251 ;--------------------------------------------------------
                                    252 ; paged external ram data
                                    253 ;--------------------------------------------------------
                                    254 	.area PSEG    (PAG,XDATA)
                                    255 ;--------------------------------------------------------
                                    256 ; external ram data
                                    257 ;--------------------------------------------------------
                                    258 	.area XSEG    (XDATA)
                                    259 ;--------------------------------------------------------
                                    260 ; absolute external ram data
                                    261 ;--------------------------------------------------------
                                    262 	.area XABS    (ABS,XDATA)
                                    263 ;--------------------------------------------------------
                                    264 ; external initialized ram data
                                    265 ;--------------------------------------------------------
                                    266 	.area XISEG   (XDATA)
                                    267 	.area HOME    (CODE)
                                    268 	.area GSINIT0 (CODE)
                                    269 	.area GSINIT1 (CODE)
                                    270 	.area GSINIT2 (CODE)
                                    271 	.area GSINIT3 (CODE)
                                    272 	.area GSINIT4 (CODE)
                                    273 	.area GSINIT5 (CODE)
                                    274 	.area GSINIT  (CODE)
                                    275 	.area GSFINAL (CODE)
                                    276 	.area CSEG    (CODE)
                                    277 ;--------------------------------------------------------
                                    278 ; interrupt vector 
                                    279 ;--------------------------------------------------------
                                    280 	.area HOME    (CODE)
      000000                        281 __interrupt_vect:
      000000 02 00 06         [24]  282 	ljmp	__sdcc_gsinit_startup
                                    283 ;--------------------------------------------------------
                                    284 ; global & static initialisations
                                    285 ;--------------------------------------------------------
                                    286 	.area HOME    (CODE)
                                    287 	.area GSINIT  (CODE)
                                    288 	.area GSFINAL (CODE)
                                    289 	.area GSINIT  (CODE)
                                    290 	.globl __sdcc_gsinit_startup
                                    291 	.globl __sdcc_program_startup
                                    292 	.globl __start__stack
                                    293 	.globl __mcs51_genXINIT
                                    294 	.globl __mcs51_genXRAMCLEAR
                                    295 	.globl __mcs51_genRAMCLEAR
                                    296 ;	test.c:5: uchar tab[8] = {0x01,0x02,0x04,0x08,0x10,0x20,0x40,0x80};
      00005F 75 08 01         [24]  297 	mov	_tab,#0x01
      000062 75 09 02         [24]  298 	mov	(_tab + 0x0001),#0x02
      000065 75 0A 04         [24]  299 	mov	(_tab + 0x0002),#0x04
      000068 75 0B 08         [24]  300 	mov	(_tab + 0x0003),#0x08
      00006B 75 0C 10         [24]  301 	mov	(_tab + 0x0004),#0x10
      00006E 75 0D 20         [24]  302 	mov	(_tab + 0x0005),#0x20
      000071 75 0E 40         [24]  303 	mov	(_tab + 0x0006),#0x40
      000074 75 0F 80         [24]  304 	mov	(_tab + 0x0007),#0x80
                                    305 	.area GSFINAL (CODE)
      000077 02 00 03         [24]  306 	ljmp	__sdcc_program_startup
                                    307 ;--------------------------------------------------------
                                    308 ; Home
                                    309 ;--------------------------------------------------------
                                    310 	.area HOME    (CODE)
                                    311 	.area HOME    (CODE)
      000003                        312 __sdcc_program_startup:
      000003 02 00 9E         [24]  313 	ljmp	_main
                                    314 ;	return from main will return to caller
                                    315 ;--------------------------------------------------------
                                    316 ; code
                                    317 ;--------------------------------------------------------
                                    318 	.area CSEG    (CODE)
                                    319 ;------------------------------------------------------------
                                    320 ;Allocation info for local variables in function 'Delay'
                                    321 ;------------------------------------------------------------
                                    322 ;xms                       Allocated to registers 
                                    323 ;i                         Allocated to registers r6 r7 
                                    324 ;j                         Allocated to registers r4 r5 
                                    325 ;------------------------------------------------------------
                                    326 ;	test.c:7: void Delay(uint xms){
                                    327 ;	-----------------------------------------
                                    328 ;	 function Delay
                                    329 ;	-----------------------------------------
      00007A                        330 _Delay:
                           000007   331 	ar7 = 0x07
                           000006   332 	ar6 = 0x06
                           000005   333 	ar5 = 0x05
                           000004   334 	ar4 = 0x04
                           000003   335 	ar3 = 0x03
                           000002   336 	ar2 = 0x02
                           000001   337 	ar1 = 0x01
                           000000   338 	ar0 = 0x00
      00007A AE 82            [24]  339 	mov	r6,dpl
      00007C AF 83            [24]  340 	mov	r7,dph
                                    341 ;	test.c:9: for(i=xms;i>0;i--)
      00007E                        342 00106$:
      00007E EE               [12]  343 	mov	a,r6
      00007F 4F               [12]  344 	orl	a,r7
      000080 60 1B            [24]  345 	jz	00108$
                                    346 ;	test.c:10: for(j=110;j>0;j--);
      000082 7C 6E            [12]  347 	mov	r4,#0x6e
      000084 7D 00            [12]  348 	mov	r5,#0x00
      000086                        349 00104$:
      000086 EC               [12]  350 	mov	a,r4
      000087 24 FF            [12]  351 	add	a,#0xff
      000089 FA               [12]  352 	mov	r2,a
      00008A ED               [12]  353 	mov	a,r5
      00008B 34 FF            [12]  354 	addc	a,#0xff
      00008D FB               [12]  355 	mov	r3,a
      00008E 8A 04            [24]  356 	mov	ar4,r2
      000090 8B 05            [24]  357 	mov	ar5,r3
      000092 EA               [12]  358 	mov	a,r2
      000093 4B               [12]  359 	orl	a,r3
      000094 70 F0            [24]  360 	jnz	00104$
                                    361 ;	test.c:9: for(i=xms;i>0;i--)
      000096 1E               [12]  362 	dec	r6
      000097 BE FF 01         [24]  363 	cjne	r6,#0xff,00133$
      00009A 1F               [12]  364 	dec	r7
      00009B                        365 00133$:
      00009B 80 E1            [24]  366 	sjmp	00106$
      00009D                        367 00108$:
                                    368 ;	test.c:11: }
      00009D 22               [24]  369 	ret
                                    370 ;------------------------------------------------------------
                                    371 ;Allocation info for local variables in function 'main'
                                    372 ;------------------------------------------------------------
                                    373 ;i                         Allocated to registers r7 
                                    374 ;------------------------------------------------------------
                                    375 ;	test.c:13: void main(){
                                    376 ;	-----------------------------------------
                                    377 ;	 function main
                                    378 ;	-----------------------------------------
      00009E                        379 _main:
                                    380 ;	test.c:16: for(i=0;i<8;i++){
      00009E                        381 00109$:
      00009E 7F 00            [12]  382 	mov	r7,#0x00
      0000A0                        383 00105$:
                                    384 ;	test.c:17: P1 = tab[i];
      0000A0 EF               [12]  385 	mov	a,r7
      0000A1 24 08            [12]  386 	add	a,#_tab
      0000A3 F9               [12]  387 	mov	r1,a
      0000A4 87 90            [24]  388 	mov	_P1,@r1
                                    389 ;	test.c:18: Delay(100);
      0000A6 90 00 64         [24]  390 	mov	dptr,#0x0064
      0000A9 C0 07            [24]  391 	push	ar7
      0000AB 12 00 7A         [24]  392 	lcall	_Delay
      0000AE D0 07            [24]  393 	pop	ar7
                                    394 ;	test.c:16: for(i=0;i<8;i++){
      0000B0 0F               [12]  395 	inc	r7
      0000B1 BF 08 00         [24]  396 	cjne	r7,#0x08,00122$
      0000B4                        397 00122$:
      0000B4 40 EA            [24]  398 	jc	00105$
                                    399 ;	test.c:21: }
      0000B6 80 E6            [24]  400 	sjmp	00109$
                                    401 	.area CSEG    (CODE)
                                    402 	.area CONST   (CODE)
                                    403 	.area XINIT   (CODE)
                                    404 	.area CABS    (ABS,CODE)
