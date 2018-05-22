#   U n i t y   S i m p l e   V R   T e l e p o r t e r  
  
 [ ! [ I M A G E   A L T   T E X T   H E R E ] ( h t t p s : / / i m g . y o u t u b e . c o m / v i / P W k 4 u v d K S U s / 0 . j p g ) ] ( h t t p s : / / w w w . y o u t u b e . c o m / w a t c h ? v = P W k 4 u v d K S U s )  
  
 S i m p l e   T e l e p o r t e r   s c r i p t   w i t h o u t   a n y   p l u g - i n   o r   d e p e n d e n c i e s .  
 A l l   s c r i p t s   a r e   a c c e s s i b l e .  
  
 *   A l l   y o u   n e e d   t o   d o   i s   :  
  
 ~ ~ ~  
 V R T e l e p o r t e r . T o g g l e D i s p l a y ( t r u e ) ;  
 V R T e l e p o r t e r . T e l e p o r t ( ) ;  
 ~ ~ ~  
  
 Y o u r   c a n   d o w n l o a d   m a n a g e d   a s s e t   f r o m   [ U n i t y   A s s e t   S t o r e ] ( h t t p s : / / a s s e t s t o r e . u n i t y . c o m / p a c k a g e s / t o o l s / i n p u t - m a n a g e m e n t / s i m p l e - v r - t e l e p o r t - 1 1 5 9 9 6 ) .  
  
 #   Q u i c k   S t a r t  
  
  
  
 # #   S e t u p  
 Y o u   c a n   f i n d   ' T e l e p o r t e r '   P r e f a b   o n   P r e f a b s   f o l d e r .  
  
 1 .   A t t a c h   T e l e p o r t e r   p r e f a b   a s   a   c h i l d   o f   g a m e   o b j e c t   w h i c h   r e p r e s e n t i n g   V R   H a n d ( o r   p o s i t i o n   w h e r e   r e n d e r   o f   p a t h   s t a r t ) .  
 2 .   A s i g n   B o d y   T r a n s f o r m   p r o p e r t y   w i t h   g a m e   o b j e c t   w h i c h   y o u   w a n t   t o   t e l e p o r t .   ( e x a m p l e :   R o o t   o f   p l a y e r   g a m e   o b j e c t )  
  
 # #   H o w   t o   c o n t r o l   V R T e l e p o r t e r  
  
 * * A l l   y o u   n e e d   t o   d o   : * *  
  
 1 .   G e t   r e f e r e n c e   o f   V R T e l e p o r t e r   o b j e c t .  
 2 .   U s e   t w o   p u b l i c   m e t h o d   o f   V R T e l e p o r t e r   s c r i p t .  
  
 ( Y o u   c a n   c h e c k   S a m p l e V R T e l e p o r t e r C o n t r o l l e r . c s   i n   S a m p l e   f o l d e r )  
  
 # # #   P u b l i c   M e t h o d s  
  
 # # # #   v o i d   T o g g l e D i s p l a y ( b o o l   a c t i v e )  
  
 -   A c t i v e   a n d   d i s p l a y   v i s u a l .  
 -   U p d a t e   P a t h   V e r t i c e s .  
 -   C h e c k   g r o u n d   p o s i t i o n .  
  
 O n c e   ` T o g g l e D i s p l a y ( t r u e ) `   i s   c a l l e d ,   V R T e l e p o r t e r   a u t o m a t i c a l l y   u p d a t e   i t ' s   a r c   p a t h   o n   e v e r y   f i x e d   u p d a t e .  
  
 ( T h i s   m e a n s   y o u   d o n ' t   n e e d   t o   c a l l   T o g g l e D i s p l a y ( T r u e )   o n   e v e r y   f r a m e   w h i l d   h o l d i n g   d o w n   b u t t o n .   J u s t   c a l l i n g   o n c e   f o r   I n p u t . G e t B u t t o n D o w n   i s   e n o u g h . )  
  
 C a l l i n g   ` T o g g l e D i s p l a y ( f a l s e ) `   w i l l   t u r n   o f f   r e n d e r e r   a n d   s t o p   u p d a t i n g   p a t h   a n d   g r o u n d   p o s i t i o n .  
  
 # # # #   v o i d   T e l e p o r t ( )  
  
 -   T e l e p o r t   b o d y T r a n s f o r m   t o   d e t e c t e d   g r o u n d   p o s i t i o n .  
  
 U s e   t h i s   w h e n   p l a y e r   r e l e a s e   i n p u t   b u t t o n .  
 ( e x a m p l e :   C a l l   T e l e p o r t   m e t h o d   w h e n   I n p u t . G e t M o u s e B u t t o n U p ( 0 )   i s   t r u e )  
  
 # #   E x a m p l e   o f   h o w   t o   c o n t r o l   V R T e l e p o r t e r  
  
 ~ ~ ~  
         p u b l i c   V R T e l e p o r t e r   t e l e p o r t e r ;  
          
         v o i d   U p d a t e   ( )   {  
  
                 i f ( I n p u t . G e t M o u s e B u t t o n D o w n ( 0 ) )  
                 {  
                         t e l e p o r t e r . T o g g l e D i s p l a y ( t r u e ) ;  
                 }  
  
                 i f ( I n p u t . G e t M o u s e B u t t o n U p ( 0 ) )  
                 {  
                         t e l e p o r t e r . T e l e p o r t ( ) ;  
                         t e l e p o r t e r . T o g g l e D i s p l a y ( f a l s e ) ;  
                 }  
         }  
 ~ ~ ~  
  
 #   P r o p e r t i e s   o f   V R T e l e p o r t e r  
 -   P o s i t i o n   M a r k e r   :   G a m e   o b j e c t   u s e d   a s   g r o u n d   p o s i t i o n   m a r k e r  
 -   B o d y   T r a n s f o r m   :   G a m e   o b j e c t   w h i c h   w i l l   b e   t e l e p o r t e d  
 -   E x c l u d e   L a y e r s   :   L a y e r s   w h i c h   y o u   d o n ' t   w a n t   t o   c h e c k  
 -   A n g l e   :   T a k e - o f f   a n g l e   o f   a r c   s t a r t   p o s i t i o n  
 -   S t r e n g t h   :   F a c t o r   f o r   h o w   f a r   a r c   g o n n a   g o  
  
  
 #   S a m p l e  
 Y o u   c a n   f i n d   q u i c k   s a m p l e   o n   S a m p l e   S c e n e .  
  
 -   S a m p l e   S c e n e   u s e   F P S C o n t r o l l e r   o f   U n i t y   S t a n d a r d   A s s e t s : : C h a r a c t e r s .  
         -   Y o u   n e e d   t o   i m p o r t   C h a r a c t e r   f r o m   [ A s s e t s ]   >   [ I m p o r t   P a c k a g e ]   >   [ C h a r a c t e r s ] ,   t o   r u n   s a m p l e   s c e n e .  
 -   S t a n d a r d   A s s e t s   i s   n o t   n e c c e s s a r y   f o r   a c t u a l   u s e ! !  
  
  
 T h e r e   i s   F P S C o n t r o l l e r   g a m e   o b j e c t   i n   t h e   S a m p l e   s c e n e .  
 Y o u   c a n   f i n d   T e l e p o r t e r   a n d   T e l e p o r t e r   C o n t r o l l e r   g a m e O b j e c t s   f r o m   F P S C o n t r o l l e r ' s   c h i l d   o b j e c t s .  
  
 -   L e f t c l i c k - h o l d   w i l l   s h o w   t h a   p a t h .  
 -   L e f t c l i c k - u p   w i l l   i n s t a n t l t y   t e l e p o r t   p l a y e r   t o   t a r g e t   p o s i t i o n .  
  
 #   H o w   t o   m o d i f y   L o o k s  
  
 J u s t   m o d i f y   m a t e r i a l   u s e d   b y   l i n e   r e n d e r e r   o f   T e l e p o r t   o b j e c t ,   a n d   m a t e r i a l   u s e d   b y   m e s h   r e n d e r e r   o f   M a r k e r   o b j e c t .  
  
 #   E T C  
 -   V R T e l e p r t e r   s c r i p t   i s   a c c e s s i b l e ,   y o u   c a n   c h a n g e   w h a t e v e r   y o u   w a n t .  
  
 L i c e n s e  
 - - - - - - -  
 [ M I T ] ( L I C E N S E ) 
