# Killing Misbehaving Processes
The challenge asks us to use to kill the /challenge/decoy process which is writing fake flags into a FIFO present at /tmp/flag_fifo. Then run /challenge/run which writes the correct flag to the same FIFO and extract it by catting the FIFO.
***

## My solve
**Flag:** `pwn.college{sVvlKioUNapQx-_1At7P3GIpib6.0FNzMDOxwCNzEzNzEzW}`

First i used ps to find the process ID of the decoy command. I tried to kill the command(PID 139) but i did not have the permission to, I then tried to kill the other PID i got(142) which killed the command. Then I ran /challenge/run which sent the flag to the FIFO(/tmp/flag_fifo). Then I started another terminal to cat the FIFO file but many decoy flags were also printed. The last flag that was sent to the FIFO was the real flag.

Terminal 1:
```
hacker@processes~killing-misbehaving-processes:~$ ps -ef | grep /challenge/decoy
root         139       1  0 05:01 ?        00:00:00 su -c exec /challenge/decoy > /tmp/flag_fifo hacker
hacker       142     139  0 05:01 ?        00:00:00 /usr/bin/python /challenge/decoy
hacker       168     157  0 05:01 pts/0    00:00:00 grep --color=auto /challenge/decoy
hacker@processes~killing-misbehaving-processes:~$ kill 139
bash: kill: (139) - Operation not permitted
hacker@processes~killing-misbehaving-processes:~$ kill 142
hacker@processes~killing-misbehaving-processes:~$ ps -ef | grep /challenge/decoy
hacker       170     157  0 05:02 pts/0    00:00:00 grep --color=auto /challenge/decoy
hacker@processes~killing-misbehaving-processes:~$ /challenge/run
Sending the flag to /tmp/flag_fifo!
```

Terminal 2:
```
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
pwn.college{5Dw715ZcoU3gGayOzhU1mfwKDKupf1OfiYs8hWXzuAbeEcy}
pwn.college{B-DQX2q1xdSiCg2iZ6-uWPAbBLlQXcLawWhrvBEKXH5xPvj}
pwn.college{VuNVLR5lej.Av-dDvX0ll.8oVoVMdrOBOwtWfFgo8NjZZ03}
pwn.college{HxyAU058tVVTrgF2jQMMxD7Ezqu75pOaXCNQckqfFweJtxj}
pwn.college{OXg8kIr6CHY7yuUypqtgne3JKSAJGAwTb5rT6KwpAWAz7Kx}
pwn.college{5HSeHFnHUUKevaPnk7BaR8xuIaPjZS608x5cns7IylBQv-E}
pwn.college{Gy6gEu08xvHDIThkcui4j5CzEF1hNoqS7AeKnPEQutkqhjD}
pwn.college{RvgHkcjXMv2KmwJ9do2y6Xs0eSoc4CMQGqnCqJbHrgQrHaW}
pwn.college{NkOmwQVR5Mc64C-ytQ6jCCzXv7EojW-Z5LkCs0LLOsnycAX}
pwn.college{8lIV7.ArBq86i8xP1tBwOAZq5sRWYDrC2yr4ThPIOO73BSj}
pwn.college{-K6syeQzQWYzvQzEk6i2HoQ9BOnY0da60QfGMhbx7YLurbt}
pwn.college{A3z96OSxO-usj7Q9E7Z5XEI8la-ZIwtw-5qfxTtd4WKuYRP}
pwn.college{5u7qNaG4jKeJwSn4y0XTkiidQ.4Z9i9y8Wyn2iBPg6M8QZ3}
pwn.college{Pfhdev61ss55tVHIShoUNcTKdjzaqeWPps2Vje.eMS15UJn}
pwn.college{Gr8z.MfsWqGty5YRfbZ3NwFcDxfqORBwd1koORQuAPnVIBr}
pwn.college{IyRpfFU2tA9GT2bLG3NPCfoOsk-hpmUwJR-y0vhoq0ZN2XW}
pwn.college{iO.foa1IkaEjvzBtTsw3qSRgdM8yQqBReKQw-D-sHT2AM9X}
pwn.college{-0S9FY9K6u-gUkGKM8oxOcTOVgdb.AI-57AR4XMgJYV8gzg}
pwn.college{bG048yeUN-RstEwA2vUGJ-9ZS2S98EA0RA1QkJlNdl1yEHc}
pwn.college{9szViEur.eSMMciqZIRaiMf6fOnTnKtcMTkZJQwM0fmKITG}
pwn.college{ySh.y0ijxsLiD011Ba7YSVqB09nt1cMGtUaxjJlCrWkl8at}
pwn.college{Cgm4icCIa8BhNvrK-7xy307zyxvJK5zCa2LnHGc-fW7oMhp}
pwn.college{NcjptyLueqzpkBY43OTrXxDqeYUb0Lp2V3pWIjAw4sdUI2R}
pwn.college{B8IF9ZelLukpSLAkdDVNCm4tDy3A-odZhHpD3MfTkCzQGs8}
pwn.college{0NSioImjMoF0i5lRhbuPUlN5nwJXA4KDHVI5JpFDonG22sz}
pwn.college{nI05WKNky9tkl6mIkmA54wi2QuQ6ce04Le6ph136JvVAmq1}
pwn.college{KhQ3EbeMtsG.8uunMgr1gtyBnCA2uiNPXya8ZnDFBAA.Rmu}
pwn.college{JM7KMYf.fCRGBugY-CFeKCm9X8vVDzikDKs.UQ7HM4ObDSz}
pwn.college{hHaLG3H15Pt-lVaGEJJh.LOANgBHmeU7ZwwVE95SFVxRQTg}
pwn.college{njFBRjWmIYWq6qBIdKfHAUPaWMsaZLUaRQ9q1Tc0CCqE3uc}
pwn.college{OQ8JRBJyay3WGIP2-r1SCrSUZALpwse8LSIx8z0HxuQw2rh}
pwn.college{YF-CjyBt22m9Xpiy0J2jnsyWUd4POvGAR7siTcPW6jrsoj-}
pwn.college{VwyMQVwp3FGEzA9M5wg3v6WE0f-gn1vIUUQhV2rWQOcebiR}
pwn.college{F30U7TAr.6BcSqrblamUtzSLsgW2TqYNCy.CWHSYnLtNhLK}
pwn.college{85jd86WhETbJa0WgtJKb1c0mFDyOvTPeCzeYwwHmjCI3AM2}
pwn.college{hVx2Psy76D8jPcIDM5C2Tlbvvzhz0VbrYa0fdO1lqCE7JSz}
pwn.college{BGLO9V-Gvg6eXp2xCm4UvybsUpNgPJ2t7fZrnyKyahwFtVU}
pwn.college{BmipKX-EPRXO75Qb8LamyftsoNZCpO6oDoDO7BN5hYxhkwl}
pwn.college{IJ213vmSuiEV9YK3Owwvc9FV-hd3AWkAzmEAyPzq2lCMkBv}
pwn.college{G10r80BjKK2Eu7Wa23YLYJ9erJPXY-yyRYYZnaQhnzHDYFM}
pwn.college{1UOeegsb9UazziuiQZEMD6UYBkZLgfaPGeXK.AI0fOxQw05}
pwn.college{F5onlpgE1-CzEH7cBNAf2lRcbNRCtsur0Y7gXXgkL1OaJp-}
pwn.college{fRKZmAfFX.08aiOTdKS0F4l5ReIWaIP-2pOWy-GZymfvHNM}
pwn.college{dVakVI9surlQSacdEi4NHNyhuQZOQKOCgFHRKr0GBHnlwub}
pwn.college{ElmRBogv8MIAYf-z0wuK7zCaAM9s484QEDFNcjzzOe.Ei69}
pwn.college{Q4MRgfrekIuI.K.MclgLN38R-02uNGjeSDMpZ5bKDB5G.cf}
pwn.college{IX6DjZ9IquVrlzClpHAm9S41cB3oZaj-ZL0P21ckkVL.xQQ}
pwn.college{Un.hHZk8VgY9GU3mYnTUZc01E-BRJ1-0IRWx.-tuQ6rBrnj}
pwn.college{gCEO7mqImZ..yQ5Mn4pQKJKeRZFc6YPF5LSIWzcP5k.OESY}
pwn.college{Qp-IUFMDVxCHgt5lrv.VTbBTin.2HgEWqw9eDTY3ywtgZUZ}
pwn.college{1im3xu0768bhYfiMXwmd6M6h5Y.bHY4vNR2XwFciHwyzJ-f}
pwn.college{NmP1hWnHAAgp5hEac1AQPMmlhBE-YEvSEB7.PN2Q9V2ioIC}
pwn.college{eXz7Vztb6XVxBljQW7k02mIBSrHGBQVAbQTxEzdlD9qu-Ng}
pwn.college{2bJVrd54HlQ15MMHso7ytJOARwA5D6d0zUN2R3k7nJhOOl8}
pwn.college{tLGT1ewBr5m4TRt8EA6ZcnhZWT.cCETfeM6ZiqjJfyzuq3o}
pwn.college{WoGUva3e0hgKvrJz1-wK6Nn.tgmPEEN.Z6UEGUiXLDI6vtY}
pwn.college{awoP6eLDWeA8mgxC6OFTT87DpNCogErFhhiDvBEIEK7PF67}
pwn.college{jbF0KSQJlM0uyLY5bW9YdVQ-wegvXWx6lxOK8L4uZKT-z9J}
pwn.college{7WfmhyCYuKk5kjJja0pxqXU1Np3UCuF8RInLiGqZHizRENJ}
pwn.college{jB6Tqx8YLrTinhhOVJzst17JbgUugRo8grEl834GB83puC8}
pwn.college{9wk.radDJ5jUbrsom4lPaEzORXtz0LQPfimkwAXh.BUKq3B}
pwn.college{wN.XgnhJIDhUT1iYfrvuqppny1Yvhm-PLM0CWPGAEbldVGM}
pwn.college{-CZ8IlRJWgwd7V8uJ.M79NOJHmHEKk4SvD9NwGm5RtRjzw-}
pwn.college{3OAC1NFoT24HXlO14WglmfN0MYyp9tI6y6Xg356Dv8cqPuL}
pwn.college{dy26wuEp1rE1ZwWSURcb.YyoanD3dD-v.ddXnQl.xcsRFfB}
pwn.college{wPRUnBcoVUAKqk5DfzvGuEoLsyXLZgLNMBS63ChkuF1J1nX}
pwn.college{WhHw81DfaLaTgNCh1QFasRMOX8GF-35Hmc35gAk506QXNU-}
pwn.college{OvQUtWBTsdPeENd3dNMslcP6SVLYAywr1D0pDgSArhk5KPU}
pwn.college{1028HaJ8LEnuFy7da7p07G1crVk96zdrt3M1mzzBtB48S3Q}
pwn.college{ahRS3WYEKDEIzF8rHONtM-5k12nTmC8futx6EH2AWIoMHSJ}
pwn.college{B2u8ag.PVAhE3sDorMrtRmR0BN0stXIZdQ4hifzecwxNXtp}
pwn.college{ewTomyjVDdy08mz-YFo62xFoRtS-ipizU98d6Ws1kYhGM1J}
pwn.college{GmCJbyakWxRi2JgZWVXyfrYNNp3tZEMmLlYSPuQRhtKn5c.}
pwn.college{B8kZXnB84cEGLXiOXNIhir0WRVMsS4VQdmoDeFdeCDqEHmX}
pwn.college{VdIGAvgbL6vLcEf0lQgUIceFU-q3xR.aT1lztUvwM3tg69R}
pwn.college{pKNYRzL0qDz8oI64wk9Fbyp2MHVtb5sTkcTr4UZ7gPLfdsx}
pwn.college{teSHoiHl2cQ1jQfR4DW9CFm1sbrhsm4XUuPGzhJdSKoWCRl}
pwn.college{BaMbR5ir9WjSZMlo2Zk55AV-RTxygiOcQ08pVAeTfSoZN22}
pwn.college{vCvsv-1nKxJN1.2i6QZvjWD4zfgZkPkTRTHGrfixi8odJkk}
pwn.college{u22THndLpR9C30HOdTgmcghwHmKOJrlFzIzg7WAuOiAQgYc}
pwn.college{ZHWp2jn.hABwNJ89a6RDLjPf1oXDmHy8pLnqnK.xzoIsZ8t}
pwn.college{WFUyBMSIhVri-xm0jgqI1jAJvcwMjd7ZNNgDa0wiTmo5utQ}
pwn.college{0w94JaWz4AUgEqkwp9SBT9tHmyVl-RZFSmHR4Ocr-rlOCdT}
pwn.college{6BTmGenBIZQcpyfpcqpDZZp8lfqcszHQFo4-qnn8q6mK.0i}
pwn.college{Mr4FQ2niEVpNYacgKOUWiu2sR52Dk.1nHKlVflD7HQyyH77}
pwn.college{B27Hdu.LfTFqeGT1BzQnfRc7YjXwkmMC43X2ZIsi1HybzkC}
pwn.college{A9LRL3.ZDaA4mEcQ79ErOmFbfvMbJXRUx0YBZHEFDStHdIg}
pwn.college{IBE5U.qIAWT0iOBkq7MFdvNSliR0mExuSJWptnKyTKhaVoA}
pwn.college{JMxYgeWjItjNJDafR42soPr6UugRJQBbR2EoDiV9YG4bdZy}
pwn.college{-A7qYyabRLvU8658q67lW7AAI5U01fadK5yJbS5ydDXti4F}
pwn.college{BwiNDiEfS35Wbe3p1unyc4Y7RLX4qMnmrsf7Y2uhh63y14B}
pwn.college{9WV6FM5nn5LkMSen0ns4exHsbZjyd4jrpNjtzIFhitDylYl}
pwn.college{GpQSPnlk1s8piySgXd0Vy1Jzt6.2uJJe4nJXBHuUsqreZUA}
pwn.college{ElVMwwOVC2ihPuAg83NsIACQxLcNFqYLsZq8Q9AxgeGPEmi}
pwn.college{AegSvoffK3b0BbeJ8CiQG1tVQSMFr-H1MHvatMMPcPpYneJ}
pwn.college{B5UDcZUvGf6Xug9E7mFV4Kielpve-Nn5psylrOdB9tg8wtJ}
pwn.college{xtLFYWXcWvW3dP.0NHgNFYxYNqIYWPY3WVTzgZn8UYFbZCz}
pwn.college{LuoKE69hBA7Tw7a88qpyr2NjxoggzGjf0bBEVhu8l-zocsN}
pwn.college{Bs5JNN6jz4SVGSzicG0s78i7NEq79ps2.oIHYUzFdY3DcLl}
pwn.college{MxsNwOekSblawehgaCGIV-VqrqJE.SJwbCwxupR0lHMPCL5}
pwn.college{GYrZqsEWSaDG0L1i13pJp2G75HLJO3GqQfomKCudmp-aG7.}
pwn.college{LNZxX.o-UYQGWhdxCEEy9o6Jp0IfVn0-81GTHulQu-GQxWq}
pwn.college{5eh8K1jzJMvAJB7.cE0wloMMmUNHwFK-1.w8sSD.uepXUhB}
pwn.college{kn2ZnrtBddY.M.CgzFVWq3T4IRWJVspL-RbZhVutlzIsz8N}
pwn.college{mwouQI3I7ziyA10BCFXie-vAFYf9qSpDy7Lx571r3WSlogg}
pwn.college{5wBMexJ.306.XaF02SuMHfGozkfS6ttiLGZLBLbRe75X.NB}
pwn.college{tVTLPYq-ug0pxX3JMM934Bake8k5w9yB8osiJSVjpYO1laF}
pwn.college{A6cuhN.pzapb.A0VC0soObHo3xy8nptWlbWUq0yWoo.1UzC}
pwn.college{bcHrq5XOO5-O0g6Am0HlUt6JlPA53zu2aMCxmIl4QCdS1CK}
pwn.college{osahglA4yO3dOkwPxvDVLo1fp5HSUKmz1hfJmErA5K8aEQ0}
pwn.college{HPgVlsmC338Bqr1WI5NRP0L-UPHClgd-botfORJCxXStiz7}
pwn.college{15MTOCUpHhAErdHydC8o4X7qvnkPOqReGq5jL7AZsRLeg0C}
pwn.college{UWCqbnyJn7miaWguOkZacG8xNElhKveVJZJLIWwisiMUfnj}
pwn.college{JgzUQD-pHItb.cN5k19OjlQyUD7GsfsgVzbUUydEZ5abSVu}
pwn.college{VRFsXK6P.aVxRuBYvetHuSfnomcMBEs2yb.mcqPepY3yPRk}
pwn.college{5tvmDyjUNMi02azFrxUVf0Dg8HXDj3Cj0nBGAsIq60I9ZTq}
pwn.college{80S0ZZQuR6D2EwcO.V-pZYHtptSao1W7kwtn-p3piNF1Nx-}
pwn.college{eFRByLt82YTLlVwlZCs0WzH4RCyjx2px4D.LGc2LCNJaEPf}
pwn.college{.Nsd13L20xsIgDnV1qpir6iL05f6NWV.bpl0W-NsopqNSu6}
pwn.college{zya8YRY9801qymWZ9Z.nRJfbGjIuKdpR77sAnw2elfINqAO}
pwn.college{XokVhRNl5tFPPKWTcTVieWMC-pjuuZI0Y9bK7A0LBXxIBLV}
pwn.college{gX8nTFyNUDmNPlQYJFKdHDsbTuPjKpV5lHdDxAibLepU96y}
pwn.college{qSdiOrhntnPEavtjUfn2U.6t0yw5iA9iyBFZr-oowvUgEd8}
pwn.college{tcAUtluEQvT8bGyYlSLduLfsNxsBTdKhj2KD6mF8RqZPny0}
pwn.college{OYPvY9wGfYBfJ0Msg94HVExoDbez4cTaINvAcc6gQCRvTvp}
pwn.college{Mb2dxI-k3gQpyNVcMD.6ydjq.iPqC1P6vYZ1TGb4OzsD5Sh}
pwn.college{QZ2bgM.WAxHlUXKP5gm8rJPhYa4USOrPBI3LquFrP4OfUZK}
pwn.college{JsjemGQWhRYHcO2.PJOGFLdv-2rJIHWRr9duNp7qFDI9RZX}
pwn.college{1m-0FHPv.c8px4QjSmLKMHsjkRadHEP5OPV7-CCbi1DWOrW}
pwn.college{eXM-UQrNe4jOdNzCk4QKBLDvJWa3.kux77yQ4MrYTY.TEzf}
pwn.college{WfaHjoc17ckjcABa88U1C6K-YYI33DmwiIJHQzLoU4tuGPG}
pwn.college{SlKC3LKzF5hblNvCrPo4dBOZZCbiuo8yV03eaPkCSKjgEeg}
pwn.college{ozb4ufWxRbdHr5JFx2tvNzaYcWfc9GVJkDVYz2Lx4Shodb-}
pwn.college{Dp.5xBVBm5v19609du297EqZ4d7fy9UUoLrk6HqXSLPFnbb}
pwn.college{sVvlKioUNapQx-_1At7P3GIpib6.0FNzMDOxwCNzEzNzEzW}
^C
```

***

## What I learned
I learned that a program cannot write to a FIFO while another file is already writing to it, so we can get a problem if a decoy program is writing to the FIFO where we need to write. So we may need to kill the decoy first. Also, decoy flags might still show up in the FIFO file even after killing the decoy file because pipes are buffered, so it might already have fake flags flowing through it which gets sent to the FIFO.

***

## References 
*No references used*