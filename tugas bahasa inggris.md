#include "crow.h"

int main() {
  crow::SimpleApp app;

  CROW_ROUTE(app, "/")([](){
    return "Hello, World!";
  });

  CROW_ROUTE(app, "/hello")([](){
    return "Halo, Dunia!";
  });

  app.port(18080).multithreaded().run();
}
