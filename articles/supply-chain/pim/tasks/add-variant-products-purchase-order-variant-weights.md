---
title: إضافة منتجات متغيرة إلى أوامر شراء باستخدام أوزان متغيرة
description: يتناول هذا الإجراء الخطوات اللازمة لاستخدام أوزان متغيرة لملء بنود أوامر الشراء تلقائيًا لكل متغير من متغيرات المنتج.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27ff3784074a36d073930ba68c8dec8b1121356e
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018274"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a><span data-ttu-id="4bed8-103">إضافة منتجات متغيرة إلى أوامر شراء باستخدام أوزان متغيرة</span><span class="sxs-lookup"><span data-stu-id="4bed8-103">Add variant products to purchase orders using variant weights</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4bed8-104">يتناول هذا الإجراء الخطوات اللازمة لاستخدام أوزان متغيرة لملء بنود أوامر الشراء تلقائيًا لكل متغير من متغيرات المنتج.</span><span class="sxs-lookup"><span data-stu-id="4bed8-104">This procedure walks through the steps for using variant weights to auto populate purchase order lines for each variant of a product.</span></span> <span data-ttu-id="4bed8-105">عند تحديد كمية المنتج التي تريد شراءها، يتم إنشاء بنود أمر الشراء لكافة المتغيرات من المنتج بالكميات المقترحة اعتمادًا على الأوزان التي تم تكوينها على متغيرات المنتج.</span><span class="sxs-lookup"><span data-stu-id="4bed8-105">When you select the quantity of the product you want to purchase, purchase order lines are created for all the variants of the product with suggested quantities based on the weights configured on the product variants.</span></span> <span data-ttu-id="4bed8-106">ولا يتضمن هذا الإجراء خطوات لتكوين قيم الأوزان على أبعاد المنتج ومتغيرات المنتج.</span><span class="sxs-lookup"><span data-stu-id="4bed8-106">This procedure doesn't include steps to configure weight values on product dimensions and product variants.</span></span> <span data-ttu-id="4bed8-107">ويستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="4bed8-107">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="4bed8-108">انتقل إلى الحسابات الدائنة > أوامر الشراء > جميع أوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="4bed8-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="4bed8-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="4bed8-109">Click New.</span></span>
3. <span data-ttu-id="4bed8-110">في الحقل "حساب المورّد‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="4bed8-110">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4bed8-111">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="4bed8-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="4bed8-112">بدّل توسيع المقطع "عام".</span><span class="sxs-lookup"><span data-stu-id="4bed8-112">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="4bed8-113">في الحقل "الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="4bed8-113">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="4bed8-114">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="4bed8-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="4bed8-115">في الحقل "المستودع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="4bed8-115">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="4bed8-116">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="4bed8-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="4bed8-117">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="4bed8-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="4bed8-118">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="4bed8-118">Click OK.</span></span>
12. <span data-ttu-id="4bed8-119">بدّل توسيع المقطع "تفاصيل البنود‬‬".</span><span class="sxs-lookup"><span data-stu-id="4bed8-119">Toggle the expansion of the Line details section.</span></span>
13. <span data-ttu-id="4bed8-120">انقر فوق علامة التبويب "المتغيرات‬".</span><span class="sxs-lookup"><span data-stu-id="4bed8-120">Click the Variants tab.</span></span>
14. <span data-ttu-id="4bed8-121">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="4bed8-121">Click Add line.</span></span>
15. <span data-ttu-id="4bed8-122">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="4bed8-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="4bed8-123">في حقل "رقم الصنف"، اكتب "0140".</span><span class="sxs-lookup"><span data-stu-id="4bed8-123">In the Item number field, type '0140'.</span></span>
17. <span data-ttu-id="4bed8-124">تعيين الكمية إلى "1000".</span><span class="sxs-lookup"><span data-stu-id="4bed8-124">Set Quantity to '1000'.</span></span>
18. <span data-ttu-id="4bed8-125">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="4bed8-125">Click Save.</span></span>

