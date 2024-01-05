FROM --platform=linux/amd64  pytorch/pytorch

# Ensures that Python output to stdout/stderr is not buffered: prevents missing information when terminating
ENV PYTHONUNBUFFERED 1

RUN adduser --system --group user
USER user

WORKDIR /tmp

COPY --chown=user:user requirements.txt /tmp

RUN python -m pip install \
    --no-color \
    --requirement requirements.txt

COPY --chown=user:user helper.py /tmp
COPY --chown=user:user inference.py /tmp

ENTRYPOINT ["python", "inference.py"]
