# SBOX-DDT-LAT

Python2 script to convert AES s-box to difference distribution table and linear approximation table


SBOX to DDT

  
    for p1 in range(256)
    
      for p2 in range(256)

        XOR_IN = p1 ^ p2

        XOR_OUT = sbox[p1] ^ sbox[p2]

        DDT[XOR_IN][XOR_OUT] += 1


SBOX to LAT

    for a in range(256)	  
    
      for b in range(256)

        for i in range(256)  

          LAT[a][b] += a.i ^ b.sbox_val[i]

        LAT[a][b]  = LAT[a][b] - 128
