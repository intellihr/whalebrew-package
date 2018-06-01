FROM python:3-alpine

RUN pip install ptpython

LABEL io.whalebrew.config.volumes '["~/.ptpython:/.ptpython"]'

ENTRYPOINT ["ptpython"]
