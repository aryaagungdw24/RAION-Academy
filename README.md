# RAION-Academy
using UnityEngine;

public class PlayerMovement : MonoBehaviour
{
    Rigidbody2D rb;
    void Start()
    {
        rb = GetComponent<Rigidbody2D>();
    }
        Vector2 Movement;
  void Update()
    {
        Movement.x = Input.GetAxisRaw("Horitzontal");
        Movement.y = Input.GetAxisRaw("Vertikal");
        Debug.Log(Movement.x + " | " + Movement.y);
        rb.MovePosition(rb.position + Movement * 1 * Time.fixedDeltaTime) ;
    }
}
