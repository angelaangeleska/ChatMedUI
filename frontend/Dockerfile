FROM node:18-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
RUN npm install recharts plotly.js react-plotly.js @mui/material @emotion/react @emotion/styled
COPY . .
RUN npm run build
RUN npm install -g serve
EXPOSE 3000
CMD ["serve", "-s", "build", "-l", "3000"]
