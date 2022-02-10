# 383.-StackPane-01
383. StackPane #01 Troca de telas com click do mouse
INICIO
________________________________________________
public class TesteStackPane extends StackPane {

	public TesteStackPane() {
		
		Caixa c1 = new Caixa().comTexto("Tela 1");
		Caixa c2 = new Caixa().comTexto("Tela 2");
		Caixa c3 = new Caixa().comTexto("Tela 3");
		Caixa c4 = new Caixa().comTexto("Tela 4");
		Caixa c5 = new Caixa().comTexto("Tela 5");
		Caixa c6 = new Caixa().comTexto("Tela 6");
		
		getChildren().addAll(c2, c3, c4, c5, c6, c1); // c1 colocado por utimo para que seja o primeiro
		
		setOnMouseClicked(e -> {
			if(e.getSceneX() > getScene().getWidth() / 2) {
			   getChildren().get(0).toFront();
			} else {
				getChildren().get(5).toBack();
			}
		});
	}
}

![image](https://user-images.githubusercontent.com/95525963/153514478-2f129cf8-9e56-4722-957a-58c6879198db.png)
