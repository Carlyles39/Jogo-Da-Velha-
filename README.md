/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package Jogos;

import javax.swing.JOptionPane;

/**
 *
 * @author carly
 */
public class JogoDaVelha extends javax.swing.JFrame {
    
    boolean Jogador1Ativo = true;
    boolean Jogador2Ativo = false;
    
    int NumeroDeVitoriaDoJogador1 = 0;
    int NumeroDeVitoriaDoJogador2 = 0;
    int NumeroDeEmpates = 0;

   
    public JogoDaVelha() {
        initComponents();
    }
    
    public void JogadorAtivo(){
        
        if(Jogador1Ativo == true){
           Jogador1Ativo = false;
           Jogador2Ativo = true;
        } else{
            Jogador1Ativo = true;
            Jogador2Ativo = false;
        }
        
        JogadorVencedor("X");
        JogadorVencedor("O");
        
    }
    
    public void JogadorVencedor(String Jogador){
        
        
        //VERIFICAR LINHAS
        if (B1.getText().equals(Jogador) &&
                B2.getText().equals(Jogador) &&
                B3.getText().equals(Jogador)) {
            if (B1.getText().equals("X")) 
                Vencedor("Jogador 1");
            else
                Vencedor("Jogador 2");
        }
        
        if (B4.getText().equals(Jogador) &&
                B5.getText().equals(Jogador) &&
                B6.getText().equals(Jogador)) {
            if (B4.getText().equals("X")) 
                Vencedor("Jogador 1");
            else
                Vencedor("Jogador 2");
        }
        
        if (B7.getText().equals(Jogador) &&
                B8.getText().equals(Jogador) &&
                B9.getText().equals(Jogador)) {
            if (B7.getText().equals("X")) 
                Vencedor("Jogador 1");
            else
                Vencedor("Jogador 2");
        }
        
        //VERIFICAR COLUNAS
        if (B1.getText().equals(Jogador) &&
                B4.getText().equals(Jogador) &&
                B7.getText().equals(Jogador)) {
            if (B1.getText().equals("X")) 
                Vencedor("Jogador 1");
            else
                Vencedor("Jogador 2");
        }
        
        if (B2.getText().equals(Jogador) &&
                B5.getText().equals(Jogador) &&
                B8.getText().equals(Jogador)) {
            if (B2.getText().equals("X")) 
                Vencedor("Jogador 1");
            else
                Vencedor("Jogador 2");
        }
        
        if (B3.getText().equals(Jogador) &&
                B6.getText().equals(Jogador) &&
                B9.getText().equals(Jogador)) {
            if (B3.getText().equals("X")) 
                Vencedor("Jogador 1");
            else
                Vencedor("Jogador 2");
        }
        
        //VERIFICAR DIAGONAIS
        if (B1.getText().equals(Jogador) &&
                B5.getText().equals(Jogador) &&
                B9.getText().equals(Jogador)) {
            if (B1.getText().equals("X")) 
                Vencedor("Jogador 1");
            else
                Vencedor("Jogador 2");
        }
        
        if (B3.getText().equals(Jogador) &&
                B5.getText().equals(Jogador) &&
                B7.getText().equals(Jogador)) {
            if (B3.getText().equals("X")) 
                Vencedor("Jogador 1");
            else
                Vencedor("Jogador 2");
        }
        
        //VERIFICAR EMPATE
        if(!B1.getText().equals("") &&
              !B2.getText().equals("") &&
              !B3.getText().equals("") &&
              !B4.getText().equals("") &&
              !B5.getText().equals("") &&
              !B6.getText().equals("") &&
              !B7.getText().equals("") &&
              !B8.getText().equals("") &&
              !B9.getText().equals("") ) {
           Vencedor("Empate");
        }
        
       
        
    }
    
    public void Vencedor(String JogadorVencedor) {
        if (JogadorVencedor.equals("Jogador 1")){
            JOptionPane.showMessageDialog(JogoDaVelha.this, "Parabéns Jogador 1!!! VOCÊ VENCEU O JOGO");
            NumeroDeVitoriaDoJogador1++;
            NumeroDeVitoriasDoJogador1.setText("Número de Vitórias: " + NumeroDeVitoriaDoJogador1);
            LimparCampos();
            
        }
        
         if (JogadorVencedor.equals("Jogador 2")){
            JOptionPane.showMessageDialog(JogoDaVelha.this, "Parabéns Jogador 2!!! VOCÊ VENCEU O JOGO");
            NumeroDeVitoriaDoJogador2++;
            NumeroDeVitoriasDoJogador2.setText("Número de Vitórias: " + NumeroDeVitoriaDoJogador2);
            LimparCampos();
        }
         
         
         if (JogadorVencedor.equals("Empate")){
             JOptionPane.showMessageDialog(JogoDaVelha.this, "Deu Empate");
             NumeroDeEmpates++;
             NumeroDeEmpate.setText("Número de Empates: " + NumeroDeEmpates);
             LimparCampos();
             
         }
        
        
    }
    
    public void LimparCampos(){
        
        B1.setText("");
        B2.setText("");
        B3.setText("");
        B4.setText("");
        B5.setText("");
        B6.setText("");
        B7.setText("");
        B8.setText("");
        B9.setText("");
        
        Jogador1Ativo = true;
        Jogador2Ativo = false;
        
        
    }

    /**
     * This method is called from within the constructor to initialize the form.
     * WARNING: Do NOT modify this code. The content of this method is always
     * regenerated by the Form Editor.
     */
    @SuppressWarnings("unchecked")
    // <editor-fold defaultstate="collapsed" desc="Generated Code">                          
    private void initComponents() {

        jPanel1 = new javax.swing.JPanel();
        B1 = new javax.swing.JButton();
        B2 = new javax.swing.JButton();
        B3 = new javax.swing.JButton();
        B4 = new javax.swing.JButton();
        B5 = new javax.swing.JButton();
        B6 = new javax.swing.JButton();
        B7 = new javax.swing.JButton();
        B8 = new javax.swing.JButton();
        B9 = new javax.swing.JButton();
        jPanel2 = new javax.swing.JPanel();
        jLabel1 = new javax.swing.JLabel();
        NumeroDeVitoriasDoJogador1 = new javax.swing.JLabel();
        jSeparator1 = new javax.swing.JSeparator();
        jLabel3 = new javax.swing.JLabel();
        NumeroDeVitoriasDoJogador2 = new javax.swing.JLabel();
        jSeparator2 = new javax.swing.JSeparator();
        NumeroDeEmpate = new javax.swing.JLabel();
        jPanel3 = new javax.swing.JPanel();
        btnNovoJogo = new javax.swing.JButton();
        btnSairdoJogo = new javax.swing.JButton();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);
        setTitle("Jogo da Velha");
        setResizable(false);

        jPanel1.setBorder(javax.swing.BorderFactory.createLineBorder(new java.awt.Color(0, 0, 0)));

        B1.setFont(new java.awt.Font("Tahoma", 0, 48)); // NOI18N
        B1.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                B1ActionPerformed(evt);
            }
        });

        B2.setFont(new java.awt.Font("Tahoma", 0, 48)); // NOI18N
        B2.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                B2ActionPerformed(evt);
            }
        });

        B3.setFont(new java.awt.Font("Tahoma", 0, 48)); // NOI18N
        B3.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                B3ActionPerformed(evt);
            }
        });

        B4.setFont(new java.awt.Font("Tahoma", 0, 48)); // NOI18N
        B4.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                B4ActionPerformed(evt);
            }
        });

        B5.setFont(new java.awt.Font("Tahoma", 0, 48)); // NOI18N
        B5.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                B5ActionPerformed(evt);
            }
        });

        B6.setFont(new java.awt.Font("Tahoma", 0, 48)); // NOI18N
        B6.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                B6ActionPerformed(evt);
            }
        });

        B7.setFont(new java.awt.Font("Tahoma", 0, 48)); // NOI18N
        B7.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                B7ActionPerformed(evt);
            }
        });

        B8.setFont(new java.awt.Font("Tahoma", 0, 48)); // NOI18N
        B8.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                B8ActionPerformed(evt);
            }
        });

        B9.setFont(new java.awt.Font("Tahoma", 0, 48)); // NOI18N
        B9.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                B9ActionPerformed(evt);
            }
        });

        javax.swing.GroupLayout jPanel1Layout = new javax.swing.GroupLayout(jPanel1);
        jPanel1.setLayout(jPanel1Layout);
        jPanel1Layout.setHorizontalGroup(
            jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(jPanel1Layout.createSequentialGroup()
                .addContainerGap()
                .addGroup(jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addGroup(jPanel1Layout.createSequentialGroup()
                        .addComponent(B1, javax.swing.GroupLayout.PREFERRED_SIZE, 100, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addComponent(B2)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addComponent(B3))
                    .addGroup(jPanel1Layout.createSequentialGroup()
                        .addComponent(B4)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addComponent(B5)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addComponent(B6))
                    .addGroup(jPanel1Layout.createSequentialGroup()
                        .addComponent(B7)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addComponent(B8)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addComponent(B9)))
                .addContainerGap(javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
        );

        jPanel1Layout.linkSize(javax.swing.SwingConstants.HORIZONTAL, new java.awt.Component[] {B1, B2, B3, B4, B5, B6, B7, B8, B9});

        jPanel1Layout.setVerticalGroup(
            jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(jPanel1Layout.createSequentialGroup()
                .addContainerGap()
                .addGroup(jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addComponent(B2)
                    .addComponent(B1, javax.swing.GroupLayout.PREFERRED_SIZE, 100, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addComponent(B3))
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                .addGroup(jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.TRAILING)
                    .addComponent(B5)
                    .addComponent(B4)
                    .addComponent(B6))
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                .addGroup(jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addComponent(B7)
                    .addComponent(B8)
                    .addComponent(B9))
                .addContainerGap(javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
        );

        jPanel1Layout.linkSize(javax.swing.SwingConstants.VERTICAL, new java.awt.Component[] {B1, B2, B3, B4, B5, B6, B7, B8, B9});

        jPanel2.setBorder(javax.swing.BorderFactory.createTitledBorder(null, "Informações do Jogo", javax.swing.border.TitledBorder.DEFAULT_JUSTIFICATION, javax.swing.border.TitledBorder.DEFAULT_POSITION, new java.awt.Font("Tahoma", 0, 12))); // NOI18N

        jLabel1.setFont(new java.awt.Font("Tahoma", 0, 12)); // NOI18N
        jLabel1.setText("Jogador 1      Símbolo: X");

        NumeroDeVitoriasDoJogador1.setFont(new java.awt.Font("Tahoma", 0, 12)); // NOI18N
        NumeroDeVitoriasDoJogador1.setText("Número de Vitórias: 0");

        jLabel3.setFont(new java.awt.Font("Tahoma", 0, 12)); // NOI18N
        jLabel3.setText("Jogador 2      Símbolo: O");

        NumeroDeVitoriasDoJogador2.setFont(new java.awt.Font("Tahoma", 0, 12)); // NOI18N
        NumeroDeVitoriasDoJogador2.setText("Número de Vitórias: 0");

        NumeroDeEmpate.setFont(new java.awt.Font("Tahoma", 0, 12)); // NOI18N
        NumeroDeEmpate.setText("Número de Empates: 0");

        javax.swing.GroupLayout jPanel2Layout = new javax.swing.GroupLayout(jPanel2);
        jPanel2.setLayout(jPanel2Layout);
        jPanel2Layout.setHorizontalGroup(
            jPanel2Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addComponent(jSeparator1)
            .addComponent(jSeparator2, javax.swing.GroupLayout.Alignment.TRAILING)
            .addGroup(jPanel2Layout.createSequentialGroup()
                .addContainerGap()
                .addGroup(jPanel2Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addComponent(jLabel1)
                    .addComponent(NumeroDeVitoriasDoJogador1)
                    .addComponent(jLabel3)
                    .addComponent(NumeroDeVitoriasDoJogador2)
                    .addComponent(NumeroDeEmpate))
                .addContainerGap(41, Short.MAX_VALUE))
        );
        jPanel2Layout.setVerticalGroup(
            jPanel2Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(jPanel2Layout.createSequentialGroup()
                .addContainerGap()
                .addComponent(jLabel1)
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.UNRELATED)
                .addComponent(NumeroDeVitoriasDoJogador1)
                .addGap(13, 13, 13)
                .addComponent(jSeparator1, javax.swing.GroupLayout.PREFERRED_SIZE, 10, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                .addComponent(jLabel3)
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.UNRELATED)
                .addComponent(NumeroDeVitoriasDoJogador2)
                .addGap(18, 18, 18)
                .addComponent(jSeparator2, javax.swing.GroupLayout.PREFERRED_SIZE, 10, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.UNRELATED)
                .addComponent(NumeroDeEmpate)
                .addContainerGap(21, Short.MAX_VALUE))
        );

        jPanel3.setBorder(javax.swing.BorderFactory.createTitledBorder(null, "Controle do Jogo", javax.swing.border.TitledBorder.DEFAULT_JUSTIFICATION, javax.swing.border.TitledBorder.DEFAULT_POSITION, new java.awt.Font("Tahoma", 0, 12))); // NOI18N

        btnNovoJogo.setText("Novo Jogo");
        btnNovoJogo.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                btnNovoJogoActionPerformed(evt);
            }
        });

        btnSairdoJogo.setText("Sair do Jogo");
        btnSairdoJogo.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                btnSairdoJogoActionPerformed(evt);
            }
        });

        javax.swing.GroupLayout jPanel3Layout = new javax.swing.GroupLayout(jPanel3);
        jPanel3.setLayout(jPanel3Layout);
        jPanel3Layout.setHorizontalGroup(
            jPanel3Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addComponent(btnNovoJogo, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
            .addComponent(btnSairdoJogo, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
        );
        jPanel3Layout.setVerticalGroup(
            jPanel3Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(jPanel3Layout.createSequentialGroup()
                .addContainerGap(javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                .addComponent(btnNovoJogo)
                .addGap(18, 18, 18)
                .addComponent(btnSairdoJogo)
                .addContainerGap())
        );

        javax.swing.GroupLayout layout = new javax.swing.GroupLayout(getContentPane());
        getContentPane().setLayout(layout);
        layout.setHorizontalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addContainerGap()
                .addComponent(jPanel1, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.UNRELATED)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING, false)
                    .addComponent(jPanel2, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                    .addComponent(jPanel3, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
                .addContainerGap(javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
        );
        layout.setVerticalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addContainerGap()
                .addComponent(jPanel2, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                .addComponent(jPanel3, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addContainerGap())
            .addGroup(javax.swing.GroupLayout.Alignment.TRAILING, layout.createSequentialGroup()
                .addContainerGap(46, Short.MAX_VALUE)
                .addComponent(jPanel1, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addGap(44, 44, 44))
        );

        pack();
    }// </editor-fold>                        

    private void B4ActionPerformed(java.awt.event.ActionEvent evt) {                                   
        
        if (Jogador1Ativo == true){
            if (B4.getText().equals("")){
                B4.setText("X");
                JogadorAtivo();
            }
        } else{
            if(B4.getText().equals("")){
               B4.setText("O");
               JogadorAtivo();
            }
        }
        
        
    }                                  

    private void B6ActionPerformed(java.awt.event.ActionEvent evt) {                                   
        
        
          if (Jogador1Ativo == true){
            if (B6.getText().equals("")){
                B6.setText("X");
                JogadorAtivo();
            }
        } else{
            if(B6.getText().equals("")){
               B6.setText("O");
               JogadorAtivo();
            }
        }
    }                                  

    private void B7ActionPerformed(java.awt.event.ActionEvent evt) {                                   
        
        
          if (Jogador1Ativo == true){
            if (B7.getText().equals("")){
                B7.setText("X");
                JogadorAtivo();
            }
        } else{
            if(B7.getText().equals("")){
               B7.setText("O");
               JogadorAtivo();
            }
        }
    }                                  

    private void B1ActionPerformed(java.awt.event.ActionEvent evt) {                                   
        
        
          if (Jogador1Ativo == true){
            if (B1.getText().equals("")){
                B1.setText("X");
                JogadorAtivo();
            }
        } else{
            if(B1.getText().equals("")){
               B1.setText("O");
               JogadorAtivo();
            }
        }
    }                                  

    private void B2ActionPerformed(java.awt.event.ActionEvent evt) {                                   
        
        
          if (Jogador1Ativo == true){
            if (B2.getText().equals("")){
                B2.setText("X");
                JogadorAtivo();
            }
        } else{
            if(B2.getText().equals("")){
               B2.setText("O");
               JogadorAtivo();
            }
        }
    }                                  

    private void B3ActionPerformed(java.awt.event.ActionEvent evt) {                                   
        
        
          if (Jogador1Ativo == true){
            if (B3.getText().equals("")){
                B3.setText("X");
                JogadorAtivo();
            }
        } else{
            if(B3.getText().equals("")){
               B3.setText("O");
               JogadorAtivo();
            }
        }
    }                                  

    private void B5ActionPerformed(java.awt.event.ActionEvent evt) {                                   
        
        
          if (Jogador1Ativo == true){
            if (B5.getText().equals("")){
                B5.setText("X");
                JogadorAtivo();
            }
        } else{
            if(B5.getText().equals("")){
               B5.setText("O");
               JogadorAtivo();
            }
        }
    }                                  

    private void B8ActionPerformed(java.awt.event.ActionEvent evt) {                                   
        
        
          if (Jogador1Ativo == true){
            if (B8.getText().equals("")){
                B8.setText("X");
                JogadorAtivo();
            }
        } else{
            if(B8.getText().equals("")){
               B8.setText("O");
               JogadorAtivo();
            }
        }
    }                                  

    private void B9ActionPerformed(java.awt.event.ActionEvent evt) {                                   
        
        
          if (Jogador1Ativo == true){
            if (B9.getText().equals("")){
                B9.setText("X");
                JogadorAtivo();
            }
        } else{
            if(B9.getText().equals("")){
               B9.setText("O");
               JogadorAtivo();
            }
        }
    }                                  

    private void btnNovoJogoActionPerformed(java.awt.event.ActionEvent evt) {                                            
        
        
        LimparCampos();
        
        
    }                                           

    private void btnSairdoJogoActionPerformed(java.awt.event.ActionEvent evt) {                                              
        
        System.exit(0);
    }                                             

    /**
     * @param args the command line arguments
     */
    public static void main(String args[]) {
        /* Set the Nimbus look and feel */
        //<editor-fold defaultstate="collapsed" desc=" Look and feel setting code (optional) ">
        /* If Nimbus (introduced in Java SE 6) is not available, stay with the default look and feel.
         * For details see http://download.oracle.com/javase/tutorial/uiswing/lookandfeel/plaf.html 
         */
        try {
            for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {
                if ("Nimbus".equals(info.getName())) {
                    javax.swing.UIManager.setLookAndFeel(info.getClassName());
                    break;
                }
            }
        } catch (ClassNotFoundException ex) {
            java.util.logging.Logger.getLogger(JogoDaVelha.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (InstantiationException ex) {
            java.util.logging.Logger.getLogger(JogoDaVelha.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (IllegalAccessException ex) {
            java.util.logging.Logger.getLogger(JogoDaVelha.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (javax.swing.UnsupportedLookAndFeelException ex) {
            java.util.logging.Logger.getLogger(JogoDaVelha.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        }
        //</editor-fold>

        /* Create and display the form */
        java.awt.EventQueue.invokeLater(new Runnable() {
            public void run() {
                new JogoDaVelha().setVisible(true);
            }
        });
    }

    // Variables declaration - do not modify                     
    private javax.swing.JButton B1;
    private javax.swing.JButton B2;
    private javax.swing.JButton B3;
    private javax.swing.JButton B4;
    private javax.swing.JButton B5;
    private javax.swing.JButton B6;
    private javax.swing.JButton B7;
    private javax.swing.JButton B8;
    private javax.swing.JButton B9;
    private javax.swing.JLabel NumeroDeEmpate;
    private javax.swing.JLabel NumeroDeVitoriasDoJogador1;
    private javax.swing.JLabel NumeroDeVitoriasDoJogador2;
    private javax.swing.JButton btnNovoJogo;
    private javax.swing.JButton btnSairdoJogo;
    private javax.swing.JLabel jLabel1;
    private javax.swing.JLabel jLabel3;
    private javax.swing.JPanel jPanel1;
    private javax.swing.JPanel jPanel2;
    private javax.swing.JPanel jPanel3;
    private javax.swing.JSeparator jSeparator1;
    private javax.swing.JSeparator jSeparator2;
    // End of variables declaration                   
}
