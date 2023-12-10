FROM ubuntu:latest
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update && apt-get install -y squid tzdata
# あとで消す
RUN apt-get install -y sudo curl ed && usermod proxy -aG sudo \ 
    && echo "50c\n%sudo   ALL=(ALL:ALL) NOPASSWD: ALL\n.\nw" | EDITOR=ed visudo

# stdout/stderrにログ出力するために、USER設定は必須
USER proxy
ENV TZ Asia/Tokyo
ENTRYPOINT ["bash", "-c"]
CMD ["squid -N"]
# CMD ["/bin/bash"]
