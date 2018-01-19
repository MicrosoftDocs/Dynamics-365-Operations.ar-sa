--- 
title: " إنشاء وربط سجلات"
description: "يوضح هذا الإجراء كيفية إنشاء سجل نقطة البيع."
author: rubencdelgado
manager: AnnBe
ms.date: 10/05/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 01a4f9988a9974ec4abdddc7062978780a15463b
ms.contentlocale: ar-sa
ms.lasthandoff: 01/19/2018

---
# <a name="create-and-associate-registers"></a><span data-ttu-id="9ccb6-103"> إنشاء وربط سجلات</span><span class="sxs-lookup"><span data-stu-id="9ccb6-103">Create and associate registers</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="9ccb6-104">يوضح هذا الإجراء كيفية إنشاء سجل نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="9ccb6-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="9ccb6-105">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="9ccb6-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="9ccb6-106">في AX7، انتقل إلى البيع بالتجزئة والتجارة > إعداد القناة > إعداد نقطة البيع > السجلات.</span><span class="sxs-lookup"><span data-stu-id="9ccb6-106">Go to Retail and commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="9ccb6-107">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="9ccb6-107">Click New.</span></span>
3. <span data-ttu-id="9ccb6-108">في الحقل "رقم السجل" اكتب معرف السجل الجديد.</span><span class="sxs-lookup"><span data-stu-id="9ccb6-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="9ccb6-109">يتضمن "معرف السجل" عادةً أكوادًا قد تساعد على تعيين السجل إلى المتجر الذي ينتمي إليه والموقع داخل المخزن.</span><span class="sxs-lookup"><span data-stu-id="9ccb6-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="9ccb6-110">في حقل "الاسم"، اكتب اسمًا وصفيًا للسجل.</span><span class="sxs-lookup"><span data-stu-id="9ccb6-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="9ccb6-111">في الحقل "رقم المتجر"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="9ccb6-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="9ccb6-112">في الحقل "ملف تعريف الأجهزة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="9ccb6-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="9ccb6-113">يتم استخدام ملفات تعريف الأجهزة لتحديد الأجهزة الطرفية للبيع بالتجزئة التي سيتم توصيلها بالسجل، مثل درج الأوراق النقدية وطابعة الإيصالات.</span><span class="sxs-lookup"><span data-stu-id="9ccb6-113">Hardware profiles are used to specify the retail peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="9ccb6-114">في حقل "ملف التعريف المرئي‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="9ccb6-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="9ccb6-115">يتم استخدام ملفات التعريف المرئية لتحديد الصور المستخدمة في خلفية نقطة البيع وصفحة تسجيل الدخول بالإضافة إلى نُسق نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="9ccb6-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="9ccb6-116">في الحقل "رقم تسجيل نقطة بيع EFT"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9ccb6-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="9ccb6-117">يتم استخدام "رقم تسجيل نقطة بيع EFT" لإعلام معالج الدفع بمحطة الدفع الطرفية التي تُرسل طلبات التفويض.</span><span class="sxs-lookup"><span data-stu-id="9ccb6-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="9ccb6-118">غالبًا ما تسمى هذه القيمة "معرف المحطة الطرفية" أو "TID".</span><span class="sxs-lookup"><span data-stu-id="9ccb6-118">This value is often called the "Terminal ID" or “TID”.</span></span> <span data-ttu-id="9ccb6-119">يمكن العثور على TID عادةً على ملصق على جهاز الدفع.</span><span class="sxs-lookup"><span data-stu-id="9ccb6-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="9ccb6-120">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="9ccb6-120">Click Save.</span></span>


