package ristinolla;

import javafx.scene.control.Button;
import javafx.scene.text.Font;
import javafx.application.Application;
import javafx.geometry.Insets;
import javafx.scene.Scene;
import javafx.scene.control.Button;
import javafx.scene.control.Label;
import javafx.scene.layout.BorderPane;
import javafx.scene.layout.GridPane;
import javafx.scene.layout.HBox;
import javafx.stage.Stage;

public class RistinollaSovellus extends Application {
    
    @Override
    public void start(Stage ikkuna) throws Exception {
    
    BorderPane asettelu = new BorderPane();
    HBox teksti = new HBox();
    GridPane ristinolla = new GridPane();
    ristinolla.setHgap(10);
    ristinolla.setVgap(10);
    String vuorossa = "x";
    Label vuoro = new Label();
    Label loppu = new Label();

    
    //Button nappi1 = new Button("");
 
    //nappi1.setFont(Font.font("Monospaced", 40));

                  
    //ristinolla.add(nappi1, 0, 0);

    int rivit = 3;
    int sarakkeet = 3;
    int[][] ristikko = new int[rivit][sarakkeet];
    
    //***KORJAA TÄMÄ OSUUS*** Siirrä button event funktio tänne
        for (int rivi = 0; rivi < ristikko.length; rivi++) {
        for (int sarake = 0; sarake < ristikko[rivi].length; sarake++) {
        //int arvo = ristikko[rivi][sarake];
        Button nappi = luoNappi(vuorossa);
        ristinolla.add(nappi, sarake, rivi);
        nappi.setOnMousePressed((event) -> {
        if(vuorossa.equals("x")) {
            nappi.setText("X");
            vaihdaVuoro(vuorossa);
            //String vuorossa2 = "o"; 
            asettelu.setTop(vuoro);
            vuoro.setText("Vuorossa: " + vuorossa);
            
        }
        else {
            nappi.setText("O");
            vaihdaVuoro(vuorossa);
            vuoro.setText("Vuorossa: " + vuorossa);
            asettelu.setTop(vuoro);

        }
    });
        }
        
    }
        
        
        
        
        
    
    
    
   
    
    
    
    asettelu.setCenter(ristinolla);
    
    
    Scene nakyma = new Scene(asettelu);
        
    ikkuna.setScene(nakyma);
    ikkuna.show();
    
    }

    private String vaihdaVuoro(String vuorossa) {
        if (vuorossa.equals("x")) {
            vuorossa.replace("x", "o");
            return vuorossa;
        }
        else {
            vuorossa.replace("o", "x");
            return vuorossa;
        }
        }
    
    
    private Button luoNappi(String vuorossa) {
        Button nappi = new Button();
        nappi.setFont(Font.font("Monospaced", 40));
        
        return nappi;
    }
    
    //Button nappi = new Button(" ");
    //nappi.setFont(Font.font("Monospaced", 40));

    public static void main(String[] args) {
        launch(RistinollaSovellus.class);
    }

}
