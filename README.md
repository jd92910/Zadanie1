# Zadanie1
1.Budowanie obrazu kontenera: docker build -f Dockerfile -t web:v1 . 
2.Uruchomienie kontenera: docker run -d -p 3000:3000 --name pogoda web:v1 
3.Informacje z logów uruchomieniowych: docker logs pogoda 
4.Liczba warstw i rozmiar obrazu: docker image inspect web:v1 --format='Liczba warstw: {{len .RootFS.Layers}}' 
                                  docker image inspect web:v1 --format='Rozmiar obrazu: {{.Size}} bajtów'
