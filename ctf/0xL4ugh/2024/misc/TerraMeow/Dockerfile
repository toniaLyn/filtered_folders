FROM kalilinux/kali-rolling
RUN apk add python3
WORKDIR /home/challenger
RUN adduser -D challenger
USER challenger
ENV TF_VAR_FLAG="0xL4ugh{F4k3_Fl4G_F0r_T4stIng}"
COPY entrypoint.sh .
COPY terraform-challenge .
COPY challenge.py .
COPY banner.py .
RUN terraform init && terraform apply -auto-approve
ENTRYPOINT ["sh","entrypoint.sh"]