# Modul-4_Struktur-Data
Sorting
Salah satu proses yang sangat penting dalam pengolahan data. Misalkan terdapat data mahasiswa, terkadang dibutuhkan data yang urut berdasarkan nilai, penghasilan orang tua .

------------------------------------------------------------------------------------------------------------------------------------------
Bubble Sort

Proses pengurutan yang secara berangsur-angsur berpindah ke posisi yang tepatkarena itulah dinamakan Bubble yang artinya gelembung.

Cara sorting bubble sort :

1.	Data dibaca mulai dari paling kiri atau mulai dari indeks ke 0 (phyton) dari suatu list data.

2.	Bandingkan antara dua buah data yang saling berdekatan (antara data ke i dan i+1), tukar posisi jika data ke-i lebih besar dibandingkan data ke-i+1 (pengurutan secara ascending).

3.	Pindah satu posisi,

4.	Melakukan perbandingan seperti langkah ke-2 dan pindah satu posisi kembali seperti langkah ke-3 sampai indeks data terakhir.

5.	Setelah langkah ke-4 dilakukan, maka data yang berada di posisi paling kanan (indeks ke-N) adalah data terbesar .

6.	Ulangi lagi langkah 1-4 dimulai dari indeks data ke 0 sampai dengan indeks ke N-1, N-2, ..., 0

    def bubbleSort(listData):
            print('Data yang akan diurutkan : ', listData)
            count=0
            for outIter in range(len(listData)-1,-1,-1):
                count=count+1
                print ('Iterasi ke-', count,':')
                for i in range(outIter):
                    if listData[i]>listData[i+1]:
                        temp=listData[i]
                        listData[i]=listData[i+1]
                        listData[i+1]=temp
                        #listData[i],listData[i+1]=listData[i+1],listData[i]
                    print(listData)
            print('Data urut-',listData)

          a=[12,0,5,1,11,20,4,2]
          bubbleSort(a)
          b=[12,11,5,1,0]
          print('--')
          bubbleSort(b)

------------------------------------------------------------------------------------------------------------------------------------------
Selection Sort
Algoritma pengurutan yang sederhana namun sangat efisien dalam penggunaanya.
Algoritma selection sort (ascending orde):
1.	Algoritma ini dimulai dari indeks awal sampai dengan indeks akhir data.

2.	Cari data dengan nilai paling minimal (dari indeks awal sampai dengan indeks akhir) melalui proses perbandingan.

3.	Letakkan data minimal ini di indeks awal.

4.	Ulangi lagi proses pencarian data paling minimal (dari indeks awal+1 sampai dengan indeks akhir, karena indeks awal sudah terisi data yang tepat).

5.	Letakkan data ini pada indeks awal+1

6.	Ulangi lagi proses pencarian data paling minimal (dari indeks awal+2 sampai dengan akhir) dan letakkan data ini pada indeks awal+2, dst..

def selectionSort(listData):
    print('Algoritma Selection Sort konvensional')
    print('Data Awal=',listData)
    for outIter in range(len(listData)-1):       
        minIndex=outIter
        for i in range(outIter+1,len(listData)):
            if listData[i]<listData[minIndex]:
                minIndex=i

        temp=listData[outIter]
        listData[outIter]=listData[minIndex]
        listData[minIndex]=temp
        print('Iterasi ke-',outIter+1,':',listData)
    print('Data Urut=',listData)
    
a=[10,2,5,8,1,20,7,12,4]
selectionSort(a)
