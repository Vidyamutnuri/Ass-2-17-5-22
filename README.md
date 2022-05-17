# Ass-2-17-5-22
Assignment-2
        n=len(arr)
        pf=[0]*n
        pf[0]=arr[0]
        for i in range(1,n):
            pf[i]=pf[i-1]+arr[i]
        for i in range(n):
            if i==0:
                lsum=0
            else:
                lsum=pf[i-1]
            rsum=pf[n-1]-pf[i]
            if lsum==rsum:
                return i
        return -1
