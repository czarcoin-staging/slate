ARG IMAGE_NAME=slate
FROM ${IMAGE_NAME} as builder

FROM busybox
COPY --from=builder /slate/build /www
EXPOSE 80
ENTRYPOINT ["httpd", "-h", "/www", "-f", "-v"]
